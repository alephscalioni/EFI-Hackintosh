# OpenCore EFI

OpenCore EFI for Aleph's AMD Hackintosh.

## Hardware

| Component | Specification |
| --- | --- |
| Processor | AMD Ryzen 7 5700X |
| Motherboard | GIGABYTE B550M AORUS |
| Graphics card | AMD Radeon RX 6600 |

## Repository structure

The EFI folders are stored directly at the repository root:

```text
.
├── APPLE/
│   └── UPDATERS/MULTIUPDATER/
├── BOOT/
│   └── BOOTx64.efi
└── OC/
    ├── ACPI/
    ├── Drivers/
    ├── Kexts/
    ├── Resources/
    ├── Tools/
    ├── OpenCore.efi
    └── config.plist
```

## Included components

### ACPI tables

`SSDT-EC`, `SSDT-GPRW`, `SSDT-HPET`, `SSDT-PLUG`, `SSDT-SBUS` and `SSDT-USBX`.

### UEFI drivers and tools

- Drivers: `AudioDxe`, `FirmwareSettingsEntry`, `HfsPlus`, `OpenCanopy`, `OpenRuntime` and `ResetNvramEntry`.
- Tool: `ControlMsrE2`.

### Kexts

Versions are taken from the bundled `Info.plist` files for the paths referenced by `config.plist`.

| Kext | Version |
| --- | --- |
| AMFIPass | 1.4.1 |
| AppleALC | 1.9.5 |
| IO80211FamilyLegacy | 12.0, build 1200.12.2b1 |
| AirPortBrcmNIC (IO80211FamilyLegacy plugin) | 14.0, build 1400.1.1 |
| IOSkywalkFamily | 1.0 |
| Lilu | 1.7.1 |
| LucyRTL8125Ethernet | 1.2.2 |
| NVMeFix | 1.1.3 |
| NootRX | 1.0.0 |
| RestrictEvents | 1.1.6 |
| USBMap | 1.1 |
| USBToolBox | Build 1.2.0 |
| VirtualSMC | 1.3.7 |
| WhateverGreen | 1.7.0 |

### Boot picker resources

Acidanthera `Chardonnay`, `GoldenGate` and `Syrah` image sets, fonts, volume labels and a boot audio file.

## Before use

- Personal SMBIOS identifiers have been cleared. Set your own identifiers before using this EFI.
- `AppleMCEReporterDisabler.kext` is referenced in `config.plist` but is missing from this backup.
