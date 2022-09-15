---
description: >-
  This document provides guidance that help you to become a part of our
  development community.
---

# 💟 Contributing Guidelines

Orochi đRNG is an open source project, licensed under Apache License 2.0, the license will maintenance your ownership.

## Fork it

You might need to navigate to [https://github.com/orochi-network/orochimaru/fork](https://github.com/orochi-network/orochimaru/fork) and fork the existing source code to your repo.

## Check current working progress

All tasks of đRNG project will be managed  here,

{% embed url="https://github.com/orgs/orochi-network/projects/2/views/1" %}
Project Management
{% endembed %}

You might need to check and pick the right task, <mark style="color:red;">unassigned</mark> tasks are awaiting for you to take.

## Syncing your project

You might need to add our repo as a remote upstream so you can pull latest changes and sync your repo with [https://github.com/orochi-network/orochimaru](https://github.com/orochi-network/orochimaru)

> **Note:** We're prefer rebase if possible, after pulled new changes please do the rebase.

## Make changes on your repo

Check out the new branch before you write your code.

```
git checkout -b <branch>
```

We use prefix and snake case to naming our branches:

* `feature/` new feature
* `bug`/ fixing a bug
* `misc/` just small tuning or unknown kind
* `doc/` document
* `ops/` DevOps related
* `test/` test or benchmark related

Branch name is usually describe which you are provide in your pull request. E.g: `Implement VRF package` can be named `feature/implement_vrf_package`

```
git push -u origin feature/implement_vrf_package
```

## Create a pull request

Now create a pull request fro your repo, E.g: `chiro:feature/implement_vrf_package -> orochi:main` Please link project and issue to your pull request.

In case, your work is under progress add the `WIP:` prefix in the pull request's title.

## Naming your commit

All commit message must describe the issue and also in present sentence, E.g: `Use higher gasfees when attempting to speedup or cancel a transaction (#11936)`

It's the best if your can put the issue number along side the description that helps to track the issue.

## Thanks

We're welcome all kind of contributions, we will make all finance records available publicly. Feel free to contribute your code <3
