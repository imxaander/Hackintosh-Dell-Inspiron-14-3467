# OpenCore EFI for Hackintosh Dell Inspiron 14 3467
This repo contains EFI files to be used in hackintoshing using OpenCore.

You can use this for reference in your EFI to be used on your own laptop of this model:
 - **Model** : Dell Inspiron 14 3467
 - **CPU** : i3 6th gen (Skylake)
 - **dGPU** : AMD R5 M420
 - **iGPU** : Intel UHD520
   
## Support
| Feature | Status | Notes |
|:-----|:----|:----|
| Audio | Working | |
| Display | Working | |
| Wifi | Not working | Qualcomm Atheros is not supported as of Oct 24, 2024 |
| Bluetooth | Not working | Qualcomm Atheros is not supported as of Oct 24, 2024 |
| Graphics | Working | using the iGPU`UHD 520`, not the dedicated`AMD R5 M420`  |
| Sleep | Broken | cant wake the laptop from sleep |

## Notes
 - This EFI uses iGPU
 - Uses layout-id `11`. Change this in plist if audio doesn't work.
    - The supported layout ids are : `3, 11, 12, 13, 15, 17, 18, 20, 21, 22, 23, 27, 28, 29, 30, 31, 37, 66, 69, 71, 80, 82, 86, 96, 99, 100, 255`
    - Please refer to these OC docs [Fixing Audio](https://dortania.github.io/OpenCore-Post-Install/universal/audio.html), [Supported Codecs](https://github.com/acidanthera/AppleALC/wiki/Supported-codecs).
 - I added horndix.kext for usb tethering; since this laptop (by default) have unsupported wifi and bluetooth card.
 - System Information
   - `<will be updated soon>`
## Tests
| SMBIOS | Version | Result | Notes |
|:--------|:-----|:---|:---|
| iMac 17,1 | Monterey |- [x] Boots <br> - [x] Installs | Works fine :)|
