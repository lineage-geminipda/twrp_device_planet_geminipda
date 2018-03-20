## TWRP device tree for Planet Gemini PDA

Add to `.repo/local_manifests/geminipda.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project name="TeamWin/android_device_planet_geminipda" path="device/planet/geminipda" remote="github" revision="android-7.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_geminipda-eng
mka recoveryimage
```
