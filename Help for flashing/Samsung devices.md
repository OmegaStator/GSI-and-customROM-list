# Flashing GSIs and Custom ROMs on samsung devices
## Warning
- Doing what will be done here will remove your warranty from existence and will fry your knox flag, do at your own risk
- It looks like some devices could get the "Custom binaries are blocked by FRP lock", please don't try to connect to a google account if you don't know how to force unlock FRP using some engeneering firmware
- Since 2015, Samsung made some devices impossible to unlock, this includes US and Canadian devices (All careers), Australian devices (Telstra and Optus), United Kingdom devices (EE and Vodafone), German devices (Deutsche Telekom and Vodafone) and Indian devices (Mostly Reliance Jio and Airtel). If you are in this case, don't panick, some devices with theses careers might be OEM unlockable, if it isn't the case, you will need to find an exploit (except MediaTek who has a sort of common exploit, you will mostly need to find a device specific exploit for Qualcomm devices)

## Unlocking the bootloader
### This will obviously not apply to devices that are impossible to unlock (see warning for more informations)
### Unlocking and going to download mode
- Go to the settings app
- Go to the "About phone" section
- Tap 7 times on the "Build number" section (skip if you are already a developer)
- Go back to the main settings page
- Go to the "Developer options" section
- Enable "OEM unlocking" and "USB debugging" 
- Reboot to download mode (for devices with home button, volume down + home + power, for devices with bixby button, volume down + bixby + power, for devices without home or bixby button, shut down your phone, then hold volume up and volume down, then plug your phone to your computer)
- Accept the warning
- Install samsung usb drivers (windows only)

### Flash through odin
- Download the reccomended Odin version for your device
- Download your custom firmware/Recovery (no you cannot flash a custom ROM or GSI through odin)
- Open Odin
- Uncheck "Auto reboot" if you are flashing a custom recovery
- Click on "AP" and select your custom firmware/recovery
- Click on "Start"
- Wait for the process to finish
- (For custom recovery) Hold volume up + power + bixby/home (or nothing if you don't have home button nor bixby) until you see the recovery logo

## Flash through Heimdall
### I don't know how the hell heimdall works, any help here would be greatful

## Flashing a GSI
### Even if you can flash from Heimdall, because of the lack of knowlege i have about it, i will only explain how to flash a GSI from a custom recovery
- Download a GSI
- Move your GSI to your phone
- Reboot to recovery
- Wipe data
- wipe system (only for clean flash or if you are switching GSIs)
- Flash your GSI
- (Optional) Flash a custom kernel
- (Optional) Flash Gaaps
- Don't flash Magisk, it can cause a bootloop
- Reboot
- Enjoy your GSI


## Flashing a custom ROM 
- Download your custom ROM
- Move your custom ROM to your phone
- Reboot to recovery
- Wipe everything except where your custom ROM is stored
- Flash your custom ROM
- (Optional) Flash Gaaps
- Reboot
- Enjoy your custom ROM


## Common problems and fixes

### My phone is stuck on the boot logo/Animation
This is a common problem with GSIs but not with custom ROMs, here are some fixes

- Format all your partitions and flash your GSI/Custom ROM again
- (Custom ROMs only) Check if it is really for your device (some devices have the same name but different codenames or different SoCs)
- (GSI only) Check if your GSI is compatible with your device (Architecture, partition type, etc...)
- (GSI only) If you done a dirty flash, try to do a clean flash
- If you have flashed Magisk, if you have, please reflash your custom ROM/GSI without Magisk, same goes for Gapps

### Can i flash a custom ROM through odin?
- If you hate yourself, yes
### Can i flash a GSI through odin?
- Same as for custom ROMs
### I have X problem in my custom ROM/GSI, can you help me?
- No, i'm here to help you, not to fix your ROM, for custom ROMs, tell about your bug to the dev. If you are on a GSI, i hope it's not a major bug because they tend to be slower or unmaintained (because of the multiple devices they support)
- Don't forget about device-specific and brand-specific issues, they are mostly known and can't be fixed most of the time (like VoLTE on samsung devices)
### I don't have a custom recovery, can i flash a GSI?
- If you know how to use heimdall, yes (just like every device with fastboot)
