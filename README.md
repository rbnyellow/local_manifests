# MaruOS 0.6 for J5 2017

### How to build ###

```bash
# Create dirs
$ mkdir maru-0.6; cd maru-0.6

# Init repo
$ repo init -u https://github.com/maruos/manifest -b maru-0.6

# Clone my local repo
$ git clone https://github.com/rbnyellow/local_manifests.git -b maru-0.6 .repo/local_manifests

# Sync
$ repo sync --force-sync -j64 #depend of your CPU

# Clone prebuilt desktop image (see the official documentation)
$ wget https://github.com/maruos/builds/releases/download/v0.6.8/maru-geb4a1b8-debian-stretch-arm64-rootfs-e990e414.tar.gz; mv maru-geb4a1b8-debian-stretch-arm64-rootfs-e990e414.tar.gz $PWD/prebuilts/desktop-rootfs.tar.gz

# Build
$ source build/envsetup.sh
$ lunch maru_j5y17lte-userdebug
$ make -j64 #depend of your CPU
$ brunch
```
