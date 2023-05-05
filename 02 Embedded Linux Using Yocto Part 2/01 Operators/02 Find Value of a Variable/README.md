# How to check the value of variable?

For configuration changes, use the following:

```shell
bitbake -e
```

This command displays variable values after the configuration files 
- local.conf
- bblayers.conf
- bitbake.conf and so forth have been parsed.

For recipe changes, use the following

```shell
bitbake recipe -e | grep VARIABLE="
```
