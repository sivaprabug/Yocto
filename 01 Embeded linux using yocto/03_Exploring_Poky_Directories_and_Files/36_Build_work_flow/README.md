# Build work flow

## Yocto/OpenEmbedded Build System Workflow

1. Developers specify architecture, policies, patches and configuration details.

2. The build system fetches and downloads the source code from the specified location 
supports downloading tarballs and source code repositories systems such as git/svn

3. extracts the sources into a local work area

4. patches are applied

5. steps for configuring and compiling the software are run

6. installs the software into a temporary staging area 
depending on the user configuration, deb/rpm/ipk binaries are generated

7. the build system generates a binary package feed that is used to create the final root file image.

8. finally generates the file system image and a customized Extensible SDK (eSDK) for application development in parallel
