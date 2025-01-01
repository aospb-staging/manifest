aosPB - Project
===========

Getting started
---------------

To get started with Android/aosPB, you'll need to get familiar with [Source Control Tools](https://source.android.com/setup/develop).

### Spinning up the environment
--------------
```bash
bash <(curl -sL https://raw.githubusercontent.com/akhilnarang/scripts/refs/heads/master/setup/android_build_env.sh)
```

Start Syncing
---------------
To start syncing, create a directory and move in that directoery with the command below.
```bash
mkdir aospb && cd aospb
```

To initialize your local repository using the aospb trees, use a command like this:
```bash
repo init -u https://github.com/aospb-project/manifest.git -b 15.2 --git-lfs
```
Alternatively in case you have limited network/disk space resources:
```bash
repo init -u https://github.com/aospb-project/manifest.git -b 15.2 --git-lfs --depth=1
```
Then to sync up:
```bash
# The -j# option specifies the number of concurrent download threads to run.
# Default sync thread count is set as 8
# In case of sync errors, you may need to adjust this value as per you need

repo sync --force-sync --no-clone-bundle --no-tags
```
Start Building
---------------
To start the building process, setup the environment by executing the below command.
```bash
source build/envsetup.sh
```
Use the below command to perform lunch action, replace *$device_codename* as required for your device. 

```bash
breakfast $device_codename
```
To start the build:
```bash
brunch $device_codename
```
**Note**: By default build type is `user`

### Credits
--------------
 * [**AOSP**](https://android.googlesource.com)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**AOSPA**](https://github.com/AOSPA)
 * [**HentaiOS**](https://github.com/hentaios)
 * [**Project Radiant**](https://github.com/ProjectRadiant)
 * [**PixelOS-AOSP**](https://github.com/PixelOS-AOSP)
 * [**StatixOS**](https://github.com/StatiXOS)
 * [**Project Pixelage**](https://github.com/ProjectPixelage)
 * [**cAOSP**](https://github.com/c0smic-Lab)
 * [**SomethingOS**](https://github.com/SomethingOS)
 * [**DerpFest-AOSP**](https://github.com/DerpFest-AOSP)
 * ... And the list never ends.