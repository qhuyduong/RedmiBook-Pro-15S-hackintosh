# macOS on RedmiBook Pro 15S (WIP)

![Ventura](./Screenshots/Ventura.png)
![Monterey](./Screenshots/Monterey.png)

## Specifications

Type | Spec
:---------|:---------
Model Name | RedmiBook Pro 15S 2021
CPU | AMD Ryzen™ 7 5800H
RAM | 16 GB 3200 MHz DDR4
Wi-Fi | Intel® Wi-Fi 6 AX200
Audio | Realtek ALC256

## macOS Update History

- ✅ macOS Ventura 13.4
- ✅ macOS Monterey 12.6.6

## What's working

Type | Status
:---------|:----------
CPU | ✅
AMD GPU Acceleration | ✅
CPU & GPU Power Management | ✅
Audio | ✅
Intel Wi-Fi | ✅
Battery Status | ✅
Shutdown / Reboot | ✅
Microphone | ✅

## What's partially working

Type | Info | Status
:---------|:---------|:----------
USB | At the moment we need to disable one of the two USB controllers, so the ports connected to it will NOT work even in other OSes, until the setting is reverted in UMAF | ⚠️
Bluetooth | Same as USB | ⚠️

## Instructions

### Pre-Installation

#### Disabling XHC1 using Smokeless UMAF

https://github.com/DavidS95/Smokeless_UMAF

## Notes

## Kexts used

Kext | Info
:---------|:---------
[AirportItlwm](https://github.com/OpenIntelWireless/itlwm) | Intel Wi-Fi support
[AMDMicrophone](https://github.com/qhuyduong/AMDMicrophone) | Microphone support for modern AMD laptops
[AMDRyzenCPUPowerManagement](https://github.com/trulyspinach/SMCAMDProcessor) | AMD CPU Power Management
[AppleALC](https://github.com/acidanthera/AppleALC) | Fixes audio
[AppleMCEReporterDisabler](https://github.com/acidanthera/bugtracker/files/3703498/AppleMCEReporterDisabler.kext.zip) | Disables AppleIntelMCEReporter which causes panics on AMD CPUs
[BlueToolFixup.kext](https://github.com/acidanthera/BrcmPatchRAM) | Patches the macOS 12+ Bluetooth stack to support third-party cards
[BrightnessKeys.kext](https://github.com/acidanthera/BrightnessKeys) | Fixes brightness keys
[FeatureUnlock](https://github.com/acidanthera/FeatureUnlock) | Fixes Continuity Camera on macOS Ventura
[IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) | Adds Bluetooth support to macOS when paired with an Intel wireless card
[IntelBTPatcher](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) | Patches bugs in macOS
[Lilu](https://github.com/acidanthera/Lilu) | Patch Engine
[**NootedRed**](https://github.com/NootInc/NootedRed) | Lilu plugin for AMD Vega iGPUs
[NVMeFix](https://github.com/acidanthera/NVMeFix) | NVMe Power Management
[RadeonSensor](https://github.com/NootInc/RadeonSensor) | Temperature readings for AMD GPUs
[RestrictEvents](https://github.com/acidanthera/RestrictEvents) | Changes CPU Name
[SMCAMDProcessor](https://github.com/trulyspinach/SMCAMDProcessor) | Companion to AMDRyzenCPUPowerManagement
[SMCBatteryManager](https://github.com/acidanthera/VirtualSMC) | Enables battery reading
[SMCLightSensor](https://github.com/acidanthera/VirtualSMC) | Ambient light sensor on laptops
[SMCRadeonGPU](https://github.com/NootInc/RadeonSensor) | Companion to RadeonSensor
[USBMap](https://dortania.github.io/OpenCore-Post-Install/usb/manual/manual.html) | USB Map
[VirtualSMC](https://github.com/acidanthera/VirtualSMC) | Advanced Apple SMC emulator in the kernel
[VoodooI2C](https://github.com/NootInc/VoodooI2C) | Enables I2C trackpads with AMD
[VoodooI2CHID](https://github.com/NootInc/VoodooI2C) | Companion to VoodooI2C
[VoodooPS2Controller](https://github.com/acidanthera/VoodooPS2) | PS/2 Keyboard support
  
## SSDTs Used
  
SSDT | Info
:---------|:---------
SSDT-ALS0 | Enables Ambient Light Sensor
SSDT-EC | Adds a fake Embedded Controller device
SSDT-HPET | Fixes IRQ conflicts
SSDT-LID0 | Fixes LID close not sleeping
SSDT-PLUG-ALT | Fixes CPU definitions
SSDT-PNLF | Fixes Backlight control
SSDT-SBUS-MCHC | Fixes AppleSMBus
SSDT-USBX | USB stuff
SSDT-XOSI | Spoof macOS to Windows for some ACPI features

## Credits

- [Dortania](https://dortania.github.io) for their awesome guides.
- [Apple](https://www.apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and most Kexts.
- [**NootInc**](https://github.com/NootInc) for all the hard work to support AMD iGPU and trackpad.
- And anyone else that helped to develop and improve hackintoshing.
