# Know if your device works great with GSIs or Custom ROMs and get help on how to flash them

This list is intended to know if GSIs or CustomROMs works great with your device

## Device GSI Ranking

### Not compatible 🚩
Talks by itself, theses devices can't install GSIs and no ROMs make it compatible (at least of what we know)

### Absolute Garbage 🍅
Devices with this ranking needs a custom ROM to make GSIs works or major features are missing or have major issues in general.

### Not really good 👎
Devices with this ranking are known for having big issues with a lot of GSIs.

### Meh 😑
Devices with this ranking don't have major issues, but still has smaller issues (like multi camera issues).

Devices with uncommon GSI architectures (like A-only type or ARM64-Binder) are more likely to get this ranking because of the lack of compatible GSIs

### Pretty good 🤗
A device with this ranking works great without any important issue and great compatibility with other GSIs

### Goated 🔥
Devices that have this rank have really great performance and no issues whatsoever. If you have one of these devices, you may consider installing a GSI.

### Uncategorized 🤔
These devices didn't have enough tests to be sure about what works and what doesn't.

---
## GSI/Custom ROM Ranking

### Don't try it 🤮
GSI/Custom ROMs with this ranking don't work great and have too much problems related to apps and hardware.

### If you have a spare device, why not 💾
Theses GSI/Custom ROMs tends to have some problems, don't try it on your main device

### Pretty good 🥰
Has great compatibitly and not a lot of issues

### Perfect 😍
Has good customization, comatibility, interface, and no big issue

### Uncategorized 🤔
These GSI/Custom ROMs didn't have enough tests to have a categorization


---
## GSI Lists
All GSIs can be listed, they are sorted by android version.

The GSI .md files will include
- Android/SDK version
- Description
- Image type available (partition arch, processor arch, VNDK type, vanilla or gapps, su or nosu...)
- Minimal VNDK version (not shown most of the time because of GSIs that don't tell about it)
- SaR type (if available)
- Links to official website
- Links to BMC/Patreon

---
## Device Lists
All devices can be listed (even the ones that are not compatible with GSI, but they will immideatly be categorized __Not compatible__ or __absolute garbage 🍅__ (if a custom ROM adds support for GSIs))

The device .md file will include
- Maximum VNDK version
- VNDK/VNDKLite
- Partition type (A-only or AB)
- Processor arch (armeabi-v7a, arm64, arm64_binder, x86,x86_64)
- Full VNDK compliant capabilities (if you have it, good news, you can install android versions that are higher than your stock one, if you don't, well you are locked down with your stock android version)


It will also include the known custom ROMs with the following tags
- [Universal] : Theses ROMs are universal to a specific chip, some devices might be excluded
- [Shared] : Theses ROMs are common between multiple devices
- [Discontinued] : The devs of this ROM officially abandoned it or it has not recieved any update in a year


## Custom ROMs list
Because of how custom ROMs works compared to GSI, they will be included into the folder of your device

The ROM .md file will include
- Android version
- Model compatibility (for devices with different models)
- ROM it's based from
- Links to official website
- Links to BMC/ Patreon

## Contributing
You can contribute to this project, to see contribution instructions, please read ___contribute.md___

## FAQ
_cricket sound..._

Well, no questions were asked for the moment, if you have a question, post an issue and select "question" in the templates