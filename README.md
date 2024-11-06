# Hackintosh-B460M-MORTAR-i5-10500-dGPU-RX5500XT

🖥️ This is a sample [OpenCore](https://dortania.github.io/OpenCore-Install-Guide/) configuration for setups with Intel i5-10500 CPU, MSI B460M MORTAR motherboard and AMD Navi 14 series GPU.

⚠️ Please consider this configuration as a reference only, any specific configuration changes are subject to the particular device setup and use cases.

## Hardware Configurations

| **Component**     | **Model**                   |
| ----------------- | --------------------------- |
| CPU               | Intel i5-10500              |
| Motherboard       | MSI MAG B460M MORTAR        |
| Memory            | Kingston 2666MHz 16G\*2     |
| Graphics Card     | AMD Radeon RX 5500 XT       |
| Wi-Fi / Bluetooth | Broadcom BCM94360CS2 (PCIe) |
| Monitor           | LG 4K Monitor (DP/HDMI)     |

## Compatibility

| **Supported macOS Build**       | **OpenCore Version**                                                                                    | **Verified** |
| ------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------ |
| macOS Sonoma 14.7.1 (23H222)    | [OC 0.9.6](https://github.com/jackson-hu1279/Hackintosh-B460M-MORTAR-i5-10500-dGPU-RX5500XT/tree/0.9.6) | ✅           |
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

## Notes

1. Need to appy root patching with [OpenCore Legacy Patcher](https://dortania.github.io/OpenCore-Legacy-Patcher/) after every fresh install or OS update for Bluetooth and Wi-Fi to be working correctly.
2. For 1080P or 2K displays, please consider setting `UIScale=1` for standard resolution.
3. For those using Ethernet connections, you may need to manually update network settings as shown below:
   ![Ethernet Setting](/docs/Ethernet%20Setting.png)
4. Most Broadcom network cards should work with this configuration, verified with Broadcom BCM94360CS2 network card only. Intel network cards may require different drivers with different configurations.
5. Since macOS introduced the limit of 15 USB ports, if you choose to use a motherboard other than the one listed above, it is strongly recommended to create a custom USB mapping. You may consider some 3rd party tools such as [USBToolBox](https://github.com/USBToolBox/tool) for such purpose.
6. Platform information has been removed from `config.plist`, you may use CorpNewt's [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) application to generate a set of SMBIOS details like below:

```
#######################################################
#               iMac20,1 SMBIOS Info                  #
#######################################################

Type:         iMac20,1
Serial:       C02XG0FDH7JY
Board Serial: C02839303QXH69FJA
SmUUID:       DBB364D6-44B2-4A02-B922-AB4396F16DA8
```

6. A valid set of SMBIOS information may be required to activate iMessage and FaceTime, linked to your Apple ID.
7. Please be cautious when sharing your `config.plist` publicly since abused SMBIOS information could result in potential issues for associated Apple ID. Feel free to use my [OC-PlatformInfo-Remover](https://github.com/jackson-hu1279/OC-PlatformInfo-Remover) script to remove relevant platform details before sharing with others.

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

## Major Kexts

| **Kext**                 | **Version** |
| ------------------------ | ----------- |
| Lilu.kext                | 1.6.7       |
| WhateverGreen.kext       | 1.6.6       |
| VirtualSMC.kext          | 1.3.2       |
| AppleALC.kext            | 1.8.7       |
| LucyRTL8125Ethernet.kext | 1.1.0       |
| NVMeFix.kext             | 1.1.1       |
