# Adding Layers

Two ways:

1. Manual: edit bblayers.conf file and add the new layer to BBLAYERS
2. Automatic:

```shell
$ bitbake-layers add-layer <path-to-new-layer>
```

```shell
$ bitbake-layers add-layer ~/Yocto_Training/source/meta-ti/
```
