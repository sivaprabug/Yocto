# PARALLEL_MAKE

- Corresponds to the -j make option
- specifies the number of processes that GNU make can run in parallel on a compilation task
- Defaults to the number of CPUs on the system

```shell

$ bitbake -e core-image-minimal | grep ^PARALLEL_MAKE=

```
