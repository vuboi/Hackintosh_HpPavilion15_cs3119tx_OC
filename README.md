# HP Pavilion 15-Cs3119tx Hackintosh
[![OpenCore Version](https://img.shields.io/badge/OpenCore-0.7.5-green.svg)](https://github.com/shivalkyra/Hp-Pavilion-15-cs3119tx-Hackintosh-OpenCore/releases/)

|[Download Release][download-link]|
|-----------------|
[![download-badge](https://img.shields.io/badge/OpenCore-0.7.5-green.svg)](https://github.com/shivalkyra/Hp-Pavilion-15-cs3119tx-Hackintosh-OpenCore/releases/ "Download status")|
   
[download-link]: https://github.com/ic005k/QtOpenCoreConfig/releases/latest "Download status"
### Before you give this EFI a try, make sure you read [this](#Generating-your-own-serial-and-Editing-ROM)!

Tested on:
| Specs | Laptop |
| --- | --- |
| CPU | Intel Core i5-1035G1 IceLake
| GPU | NVIDIA GeForce MX250 (Disable)
| RAM | 12 GB 2666 MHz DDR4 
| SSD | 256 GB KIOXIA NVme
| Screen | Full HD (1920 x 1080) IPS
| WiFi | Update(...)
| Bluetooth | Update(...)
| Audio | Realtek ALC295
| OS | macOS Monterey 12.0.1 |
| BIOS | Update(...) |

## What works?
- Audio
- Brightness control
- Battery readout
- Wifi (Stock Wifi)
- Ethernet
- Power Management
- Keyboard + Trackpad
- Sleep
- Sleep through closing the lid
- Type C (Audio, Data transmission)
- Etc...
## What doesn't work?
- SD-Card (Not Test): You can try
- HDMI Port (Not Support IceLake Now)
- Type C HDMI (Not Test)
- ...
## Download and Install
Go to the [Releases](https://github.com/SkyrilHD/HP-8570W-Hackintosh/releases/) page of this repo and download the latest release. Then, copy the EFI folder to your EFI partition... That's it.

## How to Install macOS Catalina

There are two ways you can install Catalina:

1. Have a working install of macOS, download the Installer from the App Store, then make a bootable Installer with createinstallmedia by using this command in Terminal.
```
sudo /Applications/Install\ macOS\ Monterey.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```
2. If you are using Windows, use [macrecovery.py](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/winblows-install.html) from the offical OpenCore release package.

After you have created a bootable Installer, copy the EFI folder to the EFI partition and install as usual (GUID Partiton Map; APFS). After the installation, mount the EFI partition of the installed OS and copy the EFI folder to its partition.
## Generating your own serial and Editing ROM

Use GenSMBIOS (https://github.com/corpnewt/GenSMBIOS) to generate a serial for MacBookPro16,2 or MacBookAir9,1

use PlistEdit Pro, Opencore Configurator or any decent plist editor to manually enter the details in the following sections of the config (as shown in the video): (SystemSerialNumber, MLB, and UUID)
+ Opencore Configurator
```
https://mackie100projects.altervista.org/download-opencore-configurator/
```
+ OC Auxiliary Tools
```
https://github.com/ic005k/QtOpenCoreConfig
```
+ Videos (Update...)

You should also put in your ethernet adapter's MAC address into the ROM section.

## WiFi
 For the full macOS experience with AirDrop, Handoff and all of that, replace the Intel WiFi card with a supported Broadcom one.

## BIOS settings
    Update....

