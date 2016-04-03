# z3735-linux-patches
## About ##
A set of patches, kernel configs and various bits of information required to build working Linux kernel for Dexp Ursus 7W (and other similar Baytrail tablets with z3735 mainly) with RTL8723BS WiFi/BT and GSL1680 touchscreen

## Patches ##
* *4.X-only* - kernel version-specific patches  
   * ubuntu - Ubuntu packaging patches
* *rtl8723bs* - patches required by WiFi driver
* *rtl8723bs_bt* - patches required by BT driver  
   * rfkill.patch - patch for sources from ```apt-get source```
   * rfkill-mainline.patch - patch for sources from main linux repo
* *undo* - patch for 4.5+, that should be reverted to get WiFi/BT working
* *intel* - three patches from [here](https://cgit.freedesktop.org/cgit/?url=~miku/drm-intel/commit/&h=rc6_test&id=7e6c3f36563d133cff5b700d9c36b12ac2a0c643), [here](https://cgit.freedesktop.org/~miku/drm-intel/commit/?h=rc6_test&id=b2f08adb19fcb18fea7cda9908fa52e2b9db5e7f), and [here](https://cgit.freedesktop.org/~miku/drm-intel/commit/?h=rc6_test&id=e564271291fa70265b53fa34c01cbb0ae6282e81)
* *testing* - audio/backlight patches from Asus T100 Google+, I don't know if theese are actually needed. Neither sound, nor backlight are working)
* *Atom-set-acpi-ipc-irq-index-to-0.patch* - patch for audio on some atom devices that use acpi-ipc-irq-index = 0 instead of 5

## Drivers ##

### Bin ###
PPA with drivers: [ppa:russianneuromancer/drivers](https://launchpad.net/~russianneuromancer/+archive/ubuntu/drivers)

### Sources ###
* Wi-Fi: [rtl8723bs](https://github.com/hadess/rtl8723bs)
* BT: [rtl8723bs_bt](https://github.com/lwfinger/rtl8723bs_bt)
* Touch: [gslx680-acpi](https://github.com/onitake/gslx680-acpi)
* Battery status:  
   * 4.4: [axpd](https://github.com/Icenowy/axpd/)  
   * 4.5+: [fork-of-axpd](https://github.com/milikhin/axpd)

## Kernel ##

Kernel with applied patches at [GoogleDrive](https://drive.google.com/folderview?id=0BzIRxogf-cVkLWdiMTRoenU5amM&usp=sharing)
