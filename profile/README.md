---
# Welcome to
  <img src="https://raw.github.com/Batik-AOSP/manifest/14/batik-aosp.png">

Batik-AOSP is an open-source custom Android ROM based on Android 14

## Credits

We would like to express our gratitude to the following projects and communities for their contributions and inspiration:

  <a href="http://www.freepik.com">Logo designed by GarryKillian</a>

 * [**AOSP**](https://android.googlesource.com)
 * [**ProtonAOSP**](https://github.com/ProtonAOSP)
 * [**DerpFest**](https://github.com/DerpFest-AOSP)
 * [**Pixys OS**](https://github.com/PixysOS)
 * [**LineageOS**](https://github.com/LineageOS)
 * [**SuperiorOS**](https://github.com/SuperiorOS)
 * [**DotOS**](https://github.com/DotOS)
 * [**PixelExperience**](https://github.com/PixelExperience)
 * [**AospExtended**](https://github.com/AospExtended)
 * [**ArrowOS**](https://github.com/ArrowOS)
 * [**MSM-Xtended**](https://github.com/Project-Xtended)
 * [**HavocOS**](https://github.com/Havoc-OS)
 * [**BootleggersROM**](https://github.com/BootleggersROM)
 * [**Evolution-X**](https://github.com/evolution-x)
 * [**OMNIROM**](https://github.com/omnirom)
 * [**AOSIP**](https://github.com/aosip)
 * [**Resurrection Remix**](https://github.com/ResurrectionRemix)
## And the all the custom ROM not mentioned above

## System Requirements

Before building Batik-AOSP, ensure that your development environment meets the following requirements:

- Approximately 400GB of available disk space.
- A computer with a minimum of 16GB RAM running Linux (recommended).
- Properly configured build environment. You can use our Akhilnarang scripts to streamline the process.

```bash
git clone https://github.com/akhilnarang/scripts
cd scripts
./setup/android_build_env.sh
```

## Getting Started

To build Batik-AOSP for your device, follow these steps:

1. Initialize the repository with our manifest:

```bash
repo init -u https://github.com/Batik-AOSP/manifest.git -b 14
```

2. Initialize syncronizing repository

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

3. Start the build

```bash
. build/envsetup.sh
lunch batik_<devicecodename>-userdebug
mka batik -j$(nproc --all)
```

---
