this is a template for creating a device page, _everything in italic will need to be replaced by the corresponding information_. __/Everything that is between slashes are indications/__

__/We do the device ranking, so don't freak out if you don't see it in this template/__

# _Device name / device codename_

## Warnings
__/If your device is known for having issues with GSI, put them here/__

__/You can also warn the users if some people are spreading misinformation like sharing tutorials asking to download the GSI with the wrong partition type/__

## General informations for GSIs
- Maxial VNDK version (including custom) : _Put the maximal VNDK version that this device can achieve with a custom ROM or stock ROM installed_ __/If you don't know about it, put "unknown", if the custom roms don't have the same handling of GSI (like different partitionning), don't include it. If the maximum achived by a custom rom is the same as stock, please put the stock value and then put next to it "(Stock)"/__
- Maximal VNDK version (not including custom) : _Put the maximum VNDK version the device can achieve on stock ROM_ 
- VNDK type : _VNDK or VNDKLite_
- Device architecture : _ARM64, armeabiV7, ARM64_binder, X86, x86_64..._
- Device partition type (on stock) : _Device partition type, A-only or AB_ __/The partititon type must be the stock one/__
- Full VNDK compliant capabilities : _If the device is fully VNDK compliant, put "Yes", if not, put "No"_ __/If you don't know about it, put "unknown", you can find it by running { adb shell cat /system/etc/ld.config./put your version letter/.txt
| grep -A 20 "[vendor]" } /__

## Tips and tricks
__/optional, only if this device has problems that can be fixed in any way/__

## Known Available ROMs
__/Here put ONLY the roms that are compatible with this device. If a compatible ROM is universal for a specific SoC, put [Universal]. If it works on other devices, put [Shared]. If it is discontinued, put [Discontinued]. A rom is considered as Discontinued if the last update was from one year or more/__

## Review
__/don't put anything here, unless you are also doing a review, in this case, follow device+gsi_review.md in /Contributors /__