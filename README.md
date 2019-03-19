## TWRP device tree for Planet Gemini PDA

Add to `.repo/local_manifests/geminipda.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project name="TeamWin/android_device_planet_geminipda" path="device/planet/geminipda" remote="github" revision="android-7.1" />
  <project name="lineage-geminipda/android_kernel_planet_mt6797" path="kernel/planet/mt6797" remote="github" revision="cm-14.1" />
</manifest>
```

Then run `repo sync` to check it out.

Apply the following gerrit change

https://gerrit.omnirom.org/#/c/android_bootable_recovery/+/27694/

To build:

```sh
. build/envsetup.sh
lunch omni_geminipda-eng
mka recoveryimage
```
