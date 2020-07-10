# LineageOS 15.1 for J5 2017

### How to build ###

```bash
# Create dirs
$ mkdir lineage-15.1; cd lineage-15.1

# Init repo
$ repo init -u https://github.com/LineageOS/android.git -b lineage-15.1

# Clone my local repo
$ git clone https://github.com/rbnyellow/local_manifests.git -b lineage-15.1 .repo/local_manifests

# Sync
$ repo sync --force-sync -j64 #depend of your CPU

# Build
$ source build/envsetup.sh
$ lunch lineage_j5y17lte-userdebug
$ make -j64 #depend of your CPU
$ brunch j5y17lte
```