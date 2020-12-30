# LineageOS 15.1 for Galaxy J5 2017

### How to build ###

```bash
# Create dirs
$ mkdir lineage-15.1; cd lineage-15.1; mkdir working_dir; cd working_dir

# Init repo
$ repo init --depth=1 -u https://github.com/LineageOS/android.git -b lineage-15.1

# Clone my local repo
$ git clone https://github.com/rbnyellow/local_manifests_j5y17lte.git -b lineage-15.1 .repo/local_manifests

# Sync
$ repo sync --no-repo-verify -c --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -j`nproc`

# Build
$ source build/envsetup.sh
$ brunch lineage_j5y17lte-userdebug
```
