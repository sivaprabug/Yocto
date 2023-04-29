# BB_NUMBER_THREADS

- Determines the number of tasks that Bitbake will perform in parallel
- Note: These tasks are related to bitbake and nothing related to compiling
- Defaults to the number of CPUs on the system

```shell
$ bitbake -e core-image-minimal | grep ^BB_NUMBER_THREADS=

```
