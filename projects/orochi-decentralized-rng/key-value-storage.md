---
description: >-
  Key Value Storage package allows our full-node to store and lookup data with
  several engines.
---

# Key Value Storage

## Interface and implementation

**DatabaseEngine** is the common interface which will be shared among its implementations, this approach will allow us to support new storage engine in the future without sacrifice the consistency.

* **LevelDbEngine**: A implementation of **DatabaseEngine** for LevelDB
* **MemoryEngine**: A implementation of **DatabaseEngine** for Memory
* **KeyValueStorage**: A implementation of **DatabaseEngine**, It's also a wrapper of **LevelDbEngine** and **MemoryEngine**

```go
type EngineType int

const (
	MemoryEngine EngineType = iota
	LevelDbEngine
)

type SupportedFeature struct {
	Atomic      bool
	Synchronous bool
	Persistent  bool
}

type EngineOption struct {
	Url  string
	Type EngineType
}

type EngineCallOption struct {
	Expired int
}

type DatabaseEngine interface {
	Open(options ...func())
	Get(key []byte) ([]byte, error)
	Put(key []byte, value []byte) bool
	Del(key []byte) error
	BatchPut(keys [][]byte, values [][]byte) []bool
	BatchGet(keys [][]byte) ([][]byte, error)
	BatchDel(keys [][]byte) error
	Option(callOptions EngineCallOption) DatabaseEngine
	Feature() SupportedFeature
	EngineType() EngineType
	Close() error
}
```

**KeyValueStorage** will wrap the engine and provide the same interface.

### Option modifier

This mechanism allows us to modify the options much more flexible

```go
type LevelDbEngine struct {
}

func (l LevelDbEngine) Open(options ...func()) {
	for _, opt := range options {
		opt()
	}
}

func LevelDbDefaultOption(option *EngineOption, url string) func() {
	return func() {
		option.Type = LEVEL_DB_ENGINE
		option.Url = url
	}
}

func LevelDbChangeDb(option *EngineOption, url string) func() {
	return func() {
		option.Url = url
	}
}

// Usage
levelDb := LevelDbEngine{}
levelDbOption := &EngineOption{}
levelDb.Open(
  LevelDbDefaultOption(levelDbOption, "/data/test.ldb"),
  LevelDbChangeDb(levelDbOption, "/data/another.ldb")
)
```

### Call Option

We allow user to set the option for the next call

```go
Option(callOptions EngineCallOption) DatabaseEngine

// Usage
levelDb.Option(EngineCallOption{Expired: 30000}).set([]byte("testGo"), []byte("AAA"))

```
