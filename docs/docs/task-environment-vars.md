---
title: Task Environment Variables
---

# Task Environment Variables

Marathon sets up some environment variables for each task it launches in
addition to those set by Mesos.

## User-defined Data

Each element of the `env` field of each task's app definition describes
an environment variable.

## Host Ports

One environment variable is set for each assigned port resource.
These are named `PORT0` through `PORT{N-1}` where `N` is the number of
assigned ports. In addition provided there is at least one assigned
port, then `PORT` has the same value as `PORT0`.

## App Metadata

- `MARATHON_APP_ID`
- `MARATHON_APP_VERSION`

## Task Metadata

- `MESOS_TASK_ID`

## Values Set by Mesos

- `MESOS_SANDBOX` (set by the Docker containerizer)  
  Path within the container to the mount point of the sandbox directory.
