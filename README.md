# 🍏 ThinkCentre M910S on Hackintosh

![macOS](https://img.shields.io/badge/macOS-Monterey_12.x-000000?style=for-the-badge&logo=apple&logoColor=white)
![OpenCore](https://img.shields.io/badge/OpenCore-Bootloader-blue?style=for-the-badge)

This repository contains the OpenCore EFI configuration required to run macOS Monterey on a **Lenovo ThinkCentre M910s** powered by an Intel Core i3-6100 (Skylake) processor.

## 📸 System Info (Neofetch)
![Neofetch](screenshot/Screen%20Shot%202026-03-06%20at%2004.40.48.png)

## ⚙️ BIOS Settings
Before booting the OpenCore USB, make sure to configure your Lenovo BIOS with the following settings:
- **Boot Mode:** UEFI
- **Secure Boot:** Disabled
- **VT-d:** Enabled
- **Intel Virtualization Technology (VM):** Enabled

## 💻 Hardware Specifications

| Component | Specification |
| :--- | :--- |
| **Model** | Lenovo ThinkCentre M910s (SFF) |
| **CPU** | Intel Core i3-6100 @ 3.70 GHz (Skylake) |
| **iGPU** | Intel HD Graphics 530 |
| **RAM** | 12GB DDR4 |
| **Storage1** | Adata SU650 250GB SSD SATA |
| **Storage2** | Seagate HDD 500GB SATA |
| **Ethernet/LAN**| Intel I219-LM |
| **Wi-Fi/BT** | None |
| **SMBIOS** | `iMac17,1` |

---

## 🟢 What's Working
- [x] iGPU Acceleration (Intel HD 530)
- [x] Audio (Speaker & Mic)
- [x] Ethernet / LAN port
- [x] USB Ports (Working perfectly with USBToolBox default configuration)
- [x] iCloud, App Store, iMessage (See disclaimer below)
- [x] Short Sleep & Wake

## 🔴 Known Issues / Not Working
- [ ] **Prolonged Sleep / Deep Sleep:** The system enters sleep and wakes up perfectly fine for short periods. However, if left in sleep mode for an extended amount of time, the system fails to wake up (black screen / unresponsive) and requires a hard reboot. *(No other bugs found so far).*

---

## ⚠️ Important Disclaimer

> **DO NOT DIRECTLY COPY-PASTE THIS EFI FOR DAILY USE!**

1. **Empty SMBIOS:** The `config.plist` file in this repository uses dummy values (`0`) for `SystemUUID`, `SystemSerialNumber`, and `MLB`. 
2. You **MUST** generate your own unique SMBIOS values using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) before logging into any Apple Services. Failure to do so may result in your Apple ID getting blacklisted.
3. Please use this EFI as a reference or starting point. Do It Yourself at Your Own Risk (DWYOR).
