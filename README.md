# Dell Latitude E7480 macOS Big Sur 11 / Monterey 12.0 (OpenCore)

<div style="align: center">
<img src="https://user-images.githubusercontent.com/66028151/139106659-df5a4237-6c56-4bdf-8f02-7bbeb89fbc4b.png">
</div>

 
## 语言 / Lanuage
[简体中文](https://github.com/Lovely-XPP/Dell-Latitude-E7480-Hackintosh/blob/main/README-cn.md)

English (Current)

## Download
[![Download from https://github.com/Lovely-XPP/Dell-Latitude-E7480-Hackintosh/releases](https://img.shields.io/badge/Download-v0.7.4.1-blue)](https://github.com/Lovely-XPP/Dell-Latitude-E7480-Hackintosh/releases)

## Infomation

<details>  
<summary><strong>Booter</strong></summary>
</br>
OpenCore 0.7.2 / 0.7.3 / 0.7.4
</details>

<details>  
<summary><strong>MacOS Supported/Tested</strong></summary>
</br>
- Big Sur 11.5.0 - 11.5.2 </br>
- Big Sur 11.6 - 11.6.1 </br>
- Monterey 12.0 - 12.0.1 </br>
</details>

<details>  
<summary><strong>My Hardware</strong></summary>
</br>

| Model              | Dell Latitude E7480                        |
|:-------------------|:-------------------------------------------|
| Processor          | Intel Core i7-7700U                        |
| Graphics           | Integrated Intel HD Graphics 620           |
| Memory             | 8GB 2133MHz DDR4 * 2                       |
| Display            | 13" 2K (2560x1440) with ELAN Touchscreen   |
| Storage            | Sandisk 1T M.2 NVMe SSD                    |
| WLAN + Bluetooth   | Broadcom BCM94360Z4                        |
| Camera             | 1920x1080 FHD Webcam                       |
| Fingerprint Reader | No                                         |
| Soundcard          | Realtek ALC256                             |
| Keyboard           | Backlit Keyboard                           |
| Trackpad           | ALPS Touchpad                              |
| microSD Card Reader| Realtek RTS525A microSD card reader        |

Tips: 
* For macOS 12 Monterey, DW1820 do not work well (can not use Airdrop, Handoff and Sidercar). Therefore I change it to BCM94360Z4 and it works well!
* Strongly recommand you to re-create USBMap.kext for your own laptop with this [tool](https://github.com/corpnewt/USBMap) 
* If you change your hardware (like wireless), re-create the USBMap.kext as well.
* It is strong recommanded that re-generate a serial number for your own laptop(needed to be check invaluable in apple.com)!
* Do not turn on `Find my mac`!

</details>

<details>  
<summary><strong>Kexts Version</strong></summary>
</br>

| Kexts          | version                        |
|:----------------|:-------------------------------------------|
|	AirportBrcmFixup	|	2.1.4|
|	AirportItlwm	|	2.1.0|
|	AirportItlwm	|	2.1.0|
|	AlpsT4USB	|	1.0.0d1|
|	AppleALC	|	1.6.5|
|	BlueToolFixup	|	2.6.1|
|	BrcmBluetoothInjector	|	2.6.1|
|	BrcmFirmwareData	|	2.6.1|
|	BrcmPatchRAM3	|	2.6.1|
|	BrightnessKeys	|	1.0.3|
|	CPUFriend	|	1.2.5|
|	CpuTscSync	|	1.0.5|
|	ECEnabler	|	1.0.2|
|	FeatureUnlock	|	1.0.4|
|	HibernationFixup	|	1.4.5|
|	IOElectrify	|	1.0.0|
|	IntelBluetoothFirmware	|	2.0.1|
|	IntelBluetoothInjector	|	2.0.1|
|	IntelMausi	|	1.0.8|
|	Lilu	|	1.5.7|
|	NVMeFix	|	1.1.0|
|	RealtekCardReader	|	0.9.7|
|	RealtekCardReaderFriend	|	1.0.0|
|	RestrictEvents	|	1.0.5|
|	SMCBatteryManager	|	1.2.7|
|	SMCDellSensors	|	1.2.7|
|	SMCLightSensor	|	1.2.7|
|	SMCProcessor	|	1.2.7|
|	SMCSuperIO	|	1.2.7|
|	USBMap	|	1.0|
|	VerbStub	|	1.0.4|
|	VirtualSMC	|	1.2.7|
|	Voodoo PS/2 Controller	|	2.2.6|
|	VoodooI2C	|	2.6.5|
|	VoodooI2CHID	|	1|
|	WhateverGreen	|	1.5.5|

</details>

## Status

<details>  
<summary><strong>What's working</strong></summary>
</br>

- [x] Intel HD 620 Graphics `incuding graphics acceleration`
- [x] All USB ports (Warn: Type-C fully support hot plug)
- [x] HDMI/Type-C display monitor Hot-Plug fully supported(Sleep/dim after lock, audio output support)
- [x] Internal camera
- [x] WiFi using [AirportBrcmFixup](https://github.com/acidanthera/AirportBrcmFixup)
- [x] Bluetooth using [BrcmFirmareData and BrcmPatchRAM3](https://github.com/acidanthera/BrcmPatchRAM)
- [x] Shutdown/ Reboot/ Sleep/ Wake (include Fn + insert and LID device to sleep)
- [x] All fn key work (You need to setting on bios first. Go to POST Behavior -> Fn Lock Options. Check Fn Lock and Lock mode disable/standard)  
- [x] Speakers and headphones jack
- [x] External mic/Headphone mic jack(Working only with Big Sur 11.6 and [combojack](https://github.com/hackintosh-stuff/ComboJack)) 
- [x] Intel Gigabit Ethernet
- [x] App Store
- [x] (unsure, associated with your apple account) iMessage and Facetime 
- [x] miniDP and HDMI with digital audio passthrough(If you experience cursor lags, try turning on and off one of the displays.)
- [x] Keyboard and Trackpad (support Multitouch gestures)
- [x] Airdrop , Handoff , Sidecar and Airplay(Airplay is only support for macOS12)
- [x] SD Card Reader using [RealtekCardReader](https://github.com/0xFireWolf/RealtekCardReader) and [RealtekCardReaderFriend](https://github.com/0xFireWolf/RealtekCardReaderFriend)

</details>

<details>  
<summary><strong>What's not working</strong></summary>
</br>

None so far.

</details>

## For Intel Wireless and Bluetooth

Now, I add a config for Intel wireless card kexts. The method to use it is as below

* Delete the existing `config.plist`
* Change `config-intel-wireless-card.plist` into `config.plist`

## ComboJack Installation

Hackintosh combojack support for alc256/alc255 from https://github.com/hackintosh-stuff/ComboJack

Follow this step:
* Clone combojack repository
* Run ComboJack_Installer/install.sh in terminal and reboot
* Done. When you attach a headphone there will be a popup asking about headphone type.

## Credits
* [Acidanthera](https://github.com/Acidanthera) for oc package and main kexts.
* [daliansky](https://github.com/daliansky) for awsome SSDTs in [OC-little](https://github.com/daliansky/OC-little).
* [Dortania](https://dortania.github.io/) for installation and other guides.
* [the-darkvoid](https://github.com/the-darkvoid) for partly solve thunderbolt(type-C) hot-plug issue in [IOElectrify](https://github.com/the-darkvoid/macOS-IOElectrify)
* [hackintosh-stuff](https://github.com/hackintosh-stuff)for support externel mic/headphone with ALC256 ：[combojack](https://github.com/hackintosh-stuff/ComboJack)
* [blankmac](https://github.com/blankmac) for trackpad with multitouch gestures in [AlpsT4USB](https://github.com/blankmac/AlpsT4USB).
* All contributors for this EFI.
