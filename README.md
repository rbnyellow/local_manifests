# LineageOS 16.0 for J5 2017

### How to build ###

```bash
# Create dirs
$ mkdir lineage-16.0; cd lineage-16.0

# Init repo
$ repo init -u https://github.com/LineageOS/android.git -b lineage-16.0

# Clone my local repo
$ git clone https://gitlab.com/rbnyellow/manifests/local_manifests.git -b lineage-16.0 .repo/local_manifests

# Sync
$ repo sync --force-sync -j64 #depend of your CPU

# Build
$ source build/envsetup.sh
$ lunch lineage_j5y17lte-userdebug
$ make -j64 #depend of your CPU
$ brunch
```