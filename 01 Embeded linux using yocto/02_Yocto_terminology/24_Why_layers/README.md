# Why need Layers?

## Layers

A collection of related recipes

or

Layers are recipe containers (folders)

Typical naming convention: meta-<layername>

Poky has the following layers:

meta, meta-poky, meta-selftest, meta-skeleton, meta-yocto-bsp

Why Layers ?

Layers provide a mechanism to isolate meta data according to functionality, for instance BSPs, distribution confi
guration, etc.

You could have a BSP layer, a GUI layer, a distro configuration, middleware, or an application
Putting your entire build into one layer limits and complicates future customization and reuse.

Example: meta-poky -- Distro metadata
meta-yocto-bsp 1-- BSP metadata

Layers allow to easily to add entire sets of meta data and/or replace sets with other sets.

meta-poky, is itself a layer applied on top of the OE-Core metadata layer, meta
