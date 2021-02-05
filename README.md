# landing-teams-working-arm-arm-reference-platforms-manifest

The following should bring support for foundation_armv8 and fvp_base.

```
mkdir <workspace>
cd <workspace>
repo init -u https://github.com/MarekBykowski/landing-teams-working-arm-arm-reference-platforms-manifest.git -m foundation-yocto.xml -b refs/tags/FOUNDATION-ARMV8-2021.01.29
repo sync -j${NUM_CPUS}
export DISTRO="poky"
export MACHINE="foundation-armv8"
source setup-environment
bitbake core-image-minimal
```
