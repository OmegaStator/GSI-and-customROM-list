# Flashing GSIs and Custom ROMs on samsung devices
## Warning
- Doing what will be done here will remove your warranty from existence and will fry your knox flag, do at your own risk
- It looks like some devices could get the "Custom binaries are blocked by FRP lock", please don't try to connect to a google account if you don't know how to force unlock FRP using some engeneering firmware
- Exept some specific ROMs/GSIs, you will loose your play integrity and the environnement will become abnormal, some apps might stop working because of that
- Since 2015, Samsung made some devices impossible to unlock, this includes US and Canadian devices (All careers), Australian devices (Telstra and Optus), United Kingdom devices (EE and Vodafone), German devices (Deutsche Telekom and Vodafone) and Indian devices (Mostly Reliance Jio and Airtel). If you are in this case, don't panick, some devices with theses careers might be OEM unlockable, if it isn't the case, you will need to find a device-specific exploit (except MediaTek who has the MTKclient exploit)
- It has been found that OneUI8 entirely removes the OEM unlock option, not depending of your country or your career, you will probably have to use an exploit to unlock the bootloader if you have OneUI8 or more 
- This tutorial is made for devices __Without__ Super.img and vbmeta, I don't know how the hell does it work, i will indicate how it works the day I understand all of this shit

## Unlocking the bootloader
### This will obviously not apply to devices that are impossible to unlock (see warning for more informations)
### Unlocking and going to download mode
- Go to the settings app
- Go to the "About phone" section
- Tap 7 times on the "Build number" section (skip if you already unlocked developper mode)
- Go back to the main settings page
- Go to the "Developer options" section
- Enable "OEM unlocking" and "USB debugging" 
- Reboot to download mode (for devices with home button, volume down + home + power, for devices with bixby button, volume down + bixby + power, for devices without home or bixby button, shut down your phone, then hold volume up and volume down, then plug your phone to your computer)
- Accept the warning

### Flash through odin (windows only)
- Install samsung usb drivers
- Download the reccomended Odin version for your device
- Download your custom firmware/Recovery (it is not reccomended to directly flash a custom ROM or GSI through odin)
    - If your recovery does not come in .tar or in .md5 format but in .img, use 7zip or any simillar software to compress it into a .tar file
- Open Odin
    - Different devices will work best with different Odin versions, for any device made after 2020, it's reccomended to use Odin 3.14.4
- Uncheck "Auto reboot" if you are flashing a custom recovery
- Click on "AP" and select your custom firmware/recovery
- Click on "Start"
- Wait for the process to finish
- Force reboot by pressing Volume down + power for 7 seconds
- (For custom recovery) Hold volume up + power + bixby/home (or nothing if you don't have home button nor bixby) until you see the recovery logo
- Once you are in the recovery, you should be good to go, booting to the recovery immediately allows the custom recovery to patch android so that it doesn't replace your custom recovery with the stock one

## Flash through Heimdall
### I don't know how the hell heimdall works, any help here would be greatful

## Flashing a GSI
### Even if you can flash from Heimdall, because of the lack of knowlege i have about it, i will only explain how to flash a GSI from a custom recovery
### When you plug your phone to your computer, you might see that the storage is smaller than what you actually have, this means that /data is encrypted, you will need to format it by following the instructions
- Download a GSI
- Move your GSI to your phone
    - You can move your GSI from your custom recovery, but some are broken and MTP won't work
- Reboot to recovery
- Go to backup
- Backup Everything except data
- Go to wipe
- Select factory reset (or format data), this will format /data and will remove encryption
- Select advanced wipe and check cache, system and data
- (depends of the device) Flash a GSI-Specific Kernel
- Flash your GSI
- (Optional) Flash Gaaps
- Reboot
- Enjoy your GSI

Additionally, if you want root with magisk, you can follow theses instructions:
- Check if your GSI doesn't already have Root, __if it does, don't try to install another root on it, it will probably break__
- Go to your favorite file manager
- Unpack your custom kernel
- Go into the subdirectory where it has been unpacked, you should see a boot.img, remember where is it stored
- Install the Magisk App and open it
- Click on "install" -> Select file to patch
- Select your boot.img file
- Magisk should patch your boot.img file and tell you where is it stored. Remember where is it stored
- Go to your custom recovery
- Flash your patched boot.img as a boot image
- Reboot and go to magisk to check if everything works correctly
    - If your system bootloops, go back to your recovery and flash your original boot.img


## Flashing a custom ROM 
- Download your custom ROM
- Move your custom ROM to your phone
- Reboot to recovery
- Wipe everything except where your custom ROM is stored
- Flash your custom ROM
- (Optional) Flash Gapps
    - Don't do it on ROMs where there is already Gapps (obviously)
- Reboot
- Enjoy your custom ROM


## Common problems and fixes

### My phone is stuck on the boot logo/Animation
This is a common problem with GSIs but not with custom ROMs, here are some fixes

- Restore what you backed up in step 4, then format all your partitions and flash your GSI/Custom ROM again
- [Custom ROMs only] Check if it is really for your device (some devices have the same name but different codenames or different SoCs e.g : Samsung S24 which has a snapdragon in most countries and Exynos in EU and Korea)
- [GSI only] Check if your GSI is compatible with your device (Architecture, partition type, etc...)
- If you have flashed Magisk, please reflash your custom ROM/GSI without Magisk, same goes for Gapps

### Can i flash a custom ROM through odin?
- Yes, but good luck
### Can i flash a GSI through odin?
- Same as for custom ROMs
### I have X problem in my custom ROM/GSI, can you help me?
- No, i'm here to help you, not to fix your ROM, for custom ROMs, tell about your bug to the dev. If you are on a GSI, i hope it's not a major bug because they tend to be slower or unmaintained (because of different are all the devices)
- Don't forget about device-specific and brand-specific issues, they are mostly known and can't be fixed most of the time (like VoLTE on samsung devices)
### I don't have a custom recovery, can i flash a GSI?
- Flashing through download mode is possible but it's really hard
- Some Samsung have Fastbootd instead of the download mode or have it aside of the download mode, but even in this case it's hard