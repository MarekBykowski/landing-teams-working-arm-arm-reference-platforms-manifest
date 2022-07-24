# landing-teams-working-arm-arm-reference-platforms-manifest

The following should bring support for fvp_base.

```
mkdir <workspace>
cd <workspace>
repo init -u https://github.com/MarekBykowski/landing-teams-working-arm-arm-reference-platforms-manifest.git -m fvp-yocto.xml -b refs/tags/BASEFVP-2020.08.06
#repo init -u https://github.com/MarekBykowski/landing-teams-working-arm-arm-reference-platforms-manifest.git -m foundation-yocto.xml -b refs/tags/FOUNDATION-ARMV8-2021.01.29
#repo init -u https://github.com/MarekBykowski/landing-teams-working-arm-arm-reference-platforms-manifest.git -m corstone700.xml -b refs/tags/CORSTONE-700-2020.12.10
repo sync -j${NUM_CPUS}
export DISTRO="poky"
export MACHINE="fvp-base"
source setup-environment
bitbake core-image-minimal
```
