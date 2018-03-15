## TWRP device tree for Planet Gemini

Add to `.repo/local_manifests/gemini.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <project name="deadman96385/android_device_planet_gemini" path="device/planet/gemini" remote="github" revision="android-7.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_gemini-eng
mka recoveryimage
```
