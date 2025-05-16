[![REUSE status](https://api.reuse.software/badge/github.com/SAP/task-execution-data-set)](https://api.reuse.software/info/github.com/SAP/task-execution-data-set)

# Task Execution Data Set

## About this project

The data sets contained in this repository comprise workload metadata of a general task execution platform. The metadata consists of statically defined properties and runtime data.

## Requirements and Setup

build-data.csv contains CI Infrastructure data about resource usage of builds.
The csv is separated by ";" the exported fields are:

atom_id: uuid of build job
time: utc timestamp of build
location: cloud location id
memory_fail_count: kernel memory alloc fail counts during build
branch: branch which has been built
buildProfile: build profile that contains architecture, compiler, optimization level info
jobs: parallel build jobs (distributed compiler)
localJobs: local parallel build jobs (on executing node)
makeType: (dbg,opt,rel) - related to buildProfile but only indicating the build Type
targets: CMake target to build
component: Project that is being built
ts_phase: building or testing phase
ts_status: successful or unstable build
cgroup: executor cgroup uuid
max_rss: peak rss memory usage during the build (Bytes)
max_cache: peak page chache usage during the build (Bytes)
memreq: empirically pre-configured memory size of build container (Megabytes)

## Support, Feedback, Contributing

This project is open to feature requests/suggestions, bug reports etc. via [GitHub issues](https://github.com/SAP/task-execution-data-set/issues). Contribution and feedback are encouraged and always welcome. For more information about how to contribute, the project structure, as well as additional contribution information, see our [Contribution Guidelines](CONTRIBUTING.md).

## Security / Disclosure
If you find any bug that may be a security problem, please follow our instructions at [in our security policy](https://github.com/SAP/task-execution-data-set/security/policy) on how to report it. Please do not create GitHub issues for security-related doubts or problems.

## Code of Conduct

We as members, contributors, and leaders pledge to make participation in our community a harassment-free experience for everyone. By participating in this project, you agree to abide by its [Code of Conduct](https://github.com/SAP/.github/blob/main/CODE_OF_CONDUCT.md) at all times.

## Licensing

Copyright 2025 SAP SE or an SAP affiliate company and task-execution-data-set contributors. Please see our [LICENSE](LICENSE) for copyright and license information. Detailed information including third-party components and their licensing/copyright information is available [via the REUSE tool](https://api.reuse.software/info/github.com/SAP/task-execution-data-set).
