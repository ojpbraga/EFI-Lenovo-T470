# EFI for Lenovo ThinkPad T470 – macOS Sequoia

This repository contains a custom EFI for installing and running macOS Sequoia on the Lenovo ThinkPad T470 using the **OpenCore 1.0.4** bootloader.

## ⚙️ Tested Hardware Specs

- **Model:** Lenovo ThinkPad T470  
- **Processor:** Intel Core i5-7200U (Kaby Lake)  
- **GPU:** Intel HD Graphics 620  
- **RAM:** 8GB DDR4  
- **Storage:** SATA SSD  
- **Display:** 14" Full HD (1920x1080)  
- **Trackpad:**
- **Wi-Fi:** Intel (working with `itlwm.kext` + HeliPort)  
- **macOS Version:** Sequoia (beta)  
- **Bootloader:** OpenCore 1.0.4  

## ✅ What Works

- [x] Graphics acceleration (QE/CI)  
- [x] Audio (AppleALC)  
- [x] Keyboard and trackpad via PS2 (fully functional)  
- [x] Trackpad gestures (with VoodooI2C + VoodooInput, if needed)  
- [x] USB ports mapped  
- [x] Sleep and wake  
- [x] Webcam  
- [x] Ethernet (IntelMausi)  
- [x] Bluetooth  
- [x] Wi-Fi (via `itlwm.kext` and HeliPort)  
- [x] Battery status  
- [x] NVRAM  
- [x] Fast boot with OpenCore  

## ❌ What Doesn’t Work / Partially Works

- [ ] Fingerprint sensor  
- [ ] SD card reader (may not work depending on macOS version)  

## 🔧 Recommended BIOS Settings

- Disable **Secure Boot**  
- Disable **Virtualization-Based Security**  
- Enable **AHCI**  
- Disable **Intel Platform Trust**  
- Enable **USB Boot**  
- Enable **UEFI Only**  

## 📦 How to Use

1. Download or clone this repository.  
2. Format your USB drive as **FAT32**.  
3. Copy the contents of the `EFI` folder to the USB’s EFI partition.  
4. Boot from the USB and select the macOS installer.  
5. After installation, copy the EFI folder to the internal disk's EFI partition.

> **Tip:** Use [ProperTree](https://github.com/corpnewt/ProperTree) to edit the `config.plist` if you want to customize this EFI.


## 🛠 Kexts Included

- `Lilu.kext`  
- `WhateverGreen.kext`  
- `AppleALC.kext`  
- `VirtualSMC.kext`  
- `SMCBatteryManager.kext`  
- `VoodooPS2Controller.kext` (PS2 keyboard and mouse)  
- `IntelMausi.kext` (Ethernet)  
- `itlwm.kext` + HeliPort (Intel Wi-Fi support)  
- `VoodooI2C.kext` + `VoodooI2CHID.kext` (for gesture support, if needed)  

## 👤 Credits

- [Lenovo ThinkPad T470 Hackintosh EFI](https://github.com/MultimediaLucario/Lenovo-ThinkPad-T470)  
- [Lenovo ThinkPad T470 Hackintosh EFI](https://github.com/nitingaury/Thinkpad-T470-EFI-Opencore)  
- Hackintosh communities on Reddit, InsanelyMac, and Hackintosh Brazil  

## ⚠️ Disclaimer

This project is provided **as-is**. Always make a full backup before making any changes. Make sure your hardware is compatible before proceeding.