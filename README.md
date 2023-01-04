starfish-sdk-x86_64
===================

# Description

This is the "starfish" toolchain that is being used by LG to compile their
webOS based firmware for their range of smart TVs.

This version, along with its sysroot dependencies, was obtained through a
legal inquiry at https://opensource.lge.com/inquiry, and extracted from the
`MR_firmware.zip` archive that can itself be found in the `webOS 5.0 JO 2.0`
archive downloadable [here](http://opensource.lge.com/product/list?page=&ctgr=005&subCtgr=006&keyword=OLED65CX5LB).

This should be the exact same toolchain as the one LG used to compile
version `04.40.20` of their LG OLED##CX### smart TVs firmware.

# Installation

```
wget https://github.com/lgstreamer/starfish-sdk-x86_64/releases/download/04.40.20/starfish-sdk-x86_64-ca9v1-toolchain-5.0.0-20191125.sh
wget https://github.com/lgstreamer/starfish-sdk-x86_64/releases/download/04.40.20/target_sysroot_dependencies.tar.gz
wget https://github.com/lgstreamer/starfish-sdk-x86_64/releases/download/04.40.20/native_sysroot_dependencies.tar.gz
chmod 755 starfish-sdk-x86_64-ca9v1-toolchain-5.0.0-20191125.sh
./starfish-sdk-x86_64-ca9v1-toolchain-5.0.0-20191125.sh
. /opt/starfish-sdk-x86_64/5.0.0-20191125/environment-setup-ca9v1-starfishmllib32-linux-gnueabi
tar xvfz target_sysroot_dependencies.tar.gz -C ${SDKTARGETSYSROOT}
tar xvfz native_sysroot_dependencies.tar.gz -C ${OECORE_NATIVE_SYSROOT}
```

# Usage

Once you have done the above once, you should be able to use the SDK by simply invoking:
```
. /opt/starfish-sdk-x86_64/5.0.0-20191125/environment-setup-ca9v1-starfishmllib32-linux-gnueabi
```
