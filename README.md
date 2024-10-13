# Hackintosh-B460M-MORTAR-i5-10500-dGPU-RX5500XT

Hackintosh EFI config for MSI B460M MORTAR + i5-10500 + RX5500XT

## Hardware Configurations

| **Component**     | **Model**                   |
| ----------------- | --------------------------- |
| CPU               | Intel i5-10500              |
| Motherboard       | MSI MAG B460M MORTAR        |
| Memory            | Kingston 2666Mhz 16G\*2     |
| Graphic Card      | AMD Radeon RX 5500 XT       |
| Wi-Fi / Bluetooth | Broadcom BCM94360CS2 (PCIe) |
| Monitor           | LG 4K Monitor (DP/HDMI)     |

## Compatibility

| **Supported macOS Build**       | **OpenCore Version**                                                                                    | **Verified** |
| ------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------ |
| macOS Sonoma 14.7 (23H124)      | [OC 0.9.6](https://github.com/jackson-hu1279/Hackintosh-B460M-MORTAR-i5-10500-dGPU-RX5500XT/tree/0.9.6) | ✅           |
| macOS Ventura 13.7 (22H123)     | [OC 0.8.9](https://github.com/jackson-hu1279/Hackintosh-B460M-MORTAR-i5-10500-dGPU-RX5500XT/tree/0.8.9) | ✅           |
| macOS Monterey 12.7.6 (21H1320) | [OC 0.7.0](https://github.com/jackson-hu1279/Hackintosh-B460M-MORTAR-i5-10500-dGPU-RX5500XT/tree/0.7.0) | ✅           |

## Supported Features

| **Feature**                    | **Supported** |
| ------------------------------ | ------------- |
| Wi-Fi / Bluetooth              | ✅            |
| AirDrop / Handoff / Continuity | ✅            |
| iMessage / FaceTime            | ✅            |
| iGPU Acceleration              | ✅            |
| Metal 3                        | ✅            |
| H264 & HEVC Decoding           | ✅            |
| 4K Display Output (DP / HDMI)  | ✅            |
| Sleep / Wake                   | ✅            |
| USB / USB-C                    | ✅            |
| Onboard Ethernet               | ✅            |
| Onboard Audio                  | ✅            |

## BIOS Settings

| **Setting**                      | **Option** |
| -------------------------------- | ---------- |
| D.T.M                            | Enabled    |
| Above 4G Memory                  | Enabled    |
| IGD Multi-Monitor                | Enabled    |
| XHCI Hand-off                    | Enabled    |
| Onboard LAN Controller           | Enabled    |
| HD Audio Controller              | Enabled    |
| Fast Boot                        | Disabled   |
| Secure Boot                      | Disabled   |
| Security Device Support          | Disabled   |
| Wake Up By USB, etc.             | Disabled   |
| SATA Mode                        | AHCI       |
| Initiate Graphic Adapter         | PEG        |
| Integrated Graphics Share Memory | 64 MB      |

## Kexts

| **Kext**                 | **Version** |
| ------------------------ | ----------- |
| Lilu.kext                | 1.6.7       |
| WhateverGreen.kext       | 1.6.6       |
| VirtualSMC.kext          | 1.3.2       |
| AppleALC.kext            | 1.8.7       |
| LucyRTL8125Ethernet.kext | 1.1.0       |
| NVMeFix.kext             | 1.1.1       |
