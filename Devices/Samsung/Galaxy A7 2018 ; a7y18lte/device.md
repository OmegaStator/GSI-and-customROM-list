# Samsung Galaxy A7 (2018) / a7y18lte

## GSI Ranking : Uncategorized 🤔

This device has not been tested enough to have a proper rank

## Warnings
- Some people on XDA are incorrectly saying that this system is A-only, while the stock ROM is on AB
- Recoveries are known for having issues with recent security patches, see _tips and tricks_ for more information

## General information
- Maxial VNDK version (including custom) : VNDK30
- Maximal VNDK version (not including custom) : VNDK29 on Android 10
- VNDK type : VNDKLite
- Device architecture : ARM64
- Device partition type (on stock) : AB
- Full VNDK compilant : Yes

## Tips and tricks
Custom recoveries are having issues with recent security patches ; if no custom recovery is installed and you are gonna install one, check in download mode your BL version, if it's 5, downgrade your BL to 2020 security patch and then install your custom recovery . __WARNING : DOWNGRADING WILL MOST LIKELY CORRUPT THE /DATA PARTITION AND SO ANDROID WILL ASK YOU TO RESET YOUR PHONE, PLEASE BACKUP ANY IMPORTANT DATA BEFORE DOING ANYTHING__

## Available ROMs
- TreeUI+
- TreeUI
- LineageOS 18.1

## review

### Ressurection Remix by @OmegaStator
- Model number : SM-A750FN/DS
- Vendor ROM StockLite A7 v1.5
- Vendor ROM link : https://xdaforums.com/t/rom-10-a750x-stocklite-a7.4594889/
- Recovery Used : PitchBlack Recovery Project 3.1.0
- GSI used : Ressurection Remix 8.7.3

#### What has been tested and __works__
- Bluetooth
- Wifi
- Apps
- Customisation

#### What has been tested and __doesn't work__
- nothing for now
#### Other issues : 
- SystemUI crashes when enabling wifi/bluetooth from the QS tiles

#### Aditionnal informations
Tested with Quantum-Quack-GSI 2.5, Magisk v28.1, LSposed, MicroG

#### What do you think about it
It's great to have a lot of customisation while still having AOSP performance, not a lot of bugs and really great in general

### LineageOS 19.1 by @OmegaStator
- Phone : Samsung Galaxy A7 (2018) / a7y18lte
- model number : SM-A750FN/DS
- Vendor ROM : Android 10 stock
- Recovery Used : PitchBlack Recovery Project 3.1.0

#### What has been tested and __works__
- Bluetooth
- Wifi
- Apps
- SMS
- Non-bluetooth calls

#### What has been tested and __doesn't work__
- nothing for now
#### Other issues : 
- System randomly bootloops because of vaultkeeper, probably a device issue
#### Aditionnal informations
Tested with Quantum-Quack-GSI 2.5, Magisk v29, LSposed and MicroG

#### What do you think about it
Basic but still does a great job