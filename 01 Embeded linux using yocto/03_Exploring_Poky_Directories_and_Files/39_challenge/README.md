# save disk space

- Yocto Build System can take a lot of disk space during build. But bitbake provides options to preserve disk space

- You can tell bitbake to delete all the source code, build files after building a particular recipe by adding the following line in local.conf file

INHERIT += "rm_work"

Disadvantage: 

Difficult to debug while build fails of any recipe.

For example, if you want to exclude bitbake deleting source code of a particular package, you can add it in RM_WORK_EXCLUDE += "recipe-name"

E.g: RM_WORK_EXCLUDE += "core-image-minimal"
