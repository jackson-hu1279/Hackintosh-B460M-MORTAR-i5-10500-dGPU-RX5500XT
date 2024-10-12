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

| **Supported macOS Build**  | **OpenCore Version**                                                                                    | **Verified** |
| -------------------------- | ------------------------------------------------------------------------------------------------------- | ------------ |
| macOS Sonoma 14.7 (23H124) | [OC 0.9.6](https://github.com/jackson-hu1279/Hackintosh-B460M-MORTAR-i5-10500-dGPU-RX5500XT/tree/0.9.6) | ✅           |

## Supported Features

| **Feature**                    | **Supported** |
| ------------------------------ | ------------- |
| Wi-Fi / Bluetooth              | ✅            |
| AirDrop / Handoff / Continuity | ✅            |
| iGPU Acceleration              | ✅            |
| Metal 3                        | ✅            |
| H264 & HEVC Decoding           | ✅            |
| 4K Display Output              | ✅            |
| Sleep / Wake                   | ✅            |
| USB / USB-C                    | ✅            |
| Onboard Ethernet               | ✅            |
| Onboard Audio                  | ✅            |

## Kexts

| **Kext**                 | **Version** |
| ------------------------ | ----------- |
| Lilu.kext                | 1.6.7       |
| WhateverGreen.kext       | 1.6.6       |
| VirtualSMC.kext          | 1.3.2       |
| AppleALC.kext            | 1.8.7       |
| LucyRTL8125Ethernet.kext | 1.1.0       |
| NVMeFix.kext             | 1.1.1       |
