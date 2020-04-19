
# qualcomm_android_monitor_mode
Qualcomm QCACLD WiFi (Android) monitor mode

[![Monitor mode](https://img.shields.io/badge/monitor%20mode-working-brightgreen.svg)](#)
[![GitHub version](https://raster.shields.io/badge/version-DEV-lightgrey.svg)](#)
[![GitHub issues](https://img.shields.io/github/issues/kimocoder/qualcomm_android_monitor_mode.svg)](https://github.com/kimocoder/qualcomm_android_monitor_mode/issues)
[![GitHub forks](https://img.shields.io/github/forks/kimocoder/qualcomm_android_monitor_mode.svg)](https://github.com/kimocoder/qualcomm_android_monitor_mode/network)
[![GitHub stars](https://img.shields.io/github/stars/kimocoder/qualcomm_android_monitor_mode.svg)](https://github.com/kimocoder/qualcomm_android_monitor_mode/stargazers)
[![Build Status](https://travis-ci.org/kimocoder/qualcomm_android_monitor_mode.svg?branch=master)](https://travis-ci.org/kimocoder/qualcomm_android_monitor_mode)
[![GitHub license](https://img.shields.io/github/license/kimocoder/qualcomm_android_monitor_mode.svg)](https://github.com/kimocoder/qualcomm_android_monitor_mode/blob/master/LICENSE)
<br>
[![Kali](https://img.shields.io/badge/Kali-supported-blue.svg)](https://www.kali.org)
[![aircrack-ng](https://img.shields.io/badge/aircrack--ng-supported-blue.svg)](https://github.com/aircrack-ng/aircrack-ng)
[![wifite2](https://img.shields.io/badge/wifite2-supported-blue.svg)](https://github.com/derv82/wifite2)


### NOTES
```sh
  An update!

  This method will work OUT-of-the-BOX, it seems someone over at CodeAurora actually flipped the switch
  on monitor mode, so the kernel patch isn't really nescessary, only for they on older/unmaintained kernels.

  Great news, less dirty tricks/patching needed.
  ```

<br><br><br>
### DEPENDENCIES
```sh
  1. A rooted Android environment.
  2. Either compile a kernel yourself (NetHunter chroot works)
  3. WiFi chipset that actually uses the QCACLD driver/firmware.
  
  Older devices/drivers would need the patch from 'files', future kernels of 4.9, 4.14, 4.19
  may have it WORKING from vendor.
  
```

<br><br>
### HowTo GeT that MONITORING !

Configure device to deliver 802.11 packets in raw mode.
Below is the example of starting monitor mode and channel settings + tcpdump

Start monitor mode on adapter
```sh
echo "4" > /sys/module/wlan/parameters/con_mode
```

Stop monitor mode on adapter
```sh
ip link set wlan0 down
echo "0" > /sys/module/wlan/parameters/con_mode
ip link set wlan0 up
```


<br><br>
### Logs / Outputs

* 'iw phy0 info' output is over [here](https://github.com/kimocoder/qualcomm_android_monitor_mode/blob/master/docs/iwphy_output.txt)


<br><br>
### Downloads / Patches
  * Android QCACLD-3.0 patch to enable monitor mode - [DOWNLOAD HERE](https://github.com/kimocoder/qualcomm_android_monitor_mode/raw/master/files/enable_monitor_mode.patch)
<br><br>


<br><br>
### Credits
* kimocoder
  * Twitter: https://twitter.com/kimocoder
  
* @Re4son
  * Url: https://github.com/Re4son

* @johanlike (DJY)
  * Url: https://github.com/johanlike

* Qualcomm
  * https://www.qualcomm.com

* CodeAurora
  * https://www.codeaurora.org
<br><br><br>



<br><br>
![Setting up a custom command](https://i.imgur.com/cTJhOTB.jpg)
<br><br>
![Running monitor mode](https://i.imgur.com/s5gzFso.jpg)
<br><br>
![Running wifite2](https://i.imgur.com/VNpiXEk.jpg)
<br><br><br><br><br><br>









