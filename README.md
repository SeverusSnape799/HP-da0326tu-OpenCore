# OpenCore (0.9.5) EFI for HP 15-da0326tu (i3-7100U / HD 620)

This is a working OpenCore EFI setup for the **HP 15-da0326tu** laptop running **macOS Ventura**. Should work with Monterey and Big Sur with minimal adjustments.

## 🔧 System Specifications

- **CPU**: Intel Core i3-7100U (Kaby Lake)
- **iGPU**: Intel HD Graphics 620
- **Audio**: Realtek ALC236
- **Trackpad**: Synaptics SMBus
- **Keyboard**: Generic PS/2 
- **WiFi**: Realtek 8723DE *(not supported)*
- **Bluetooth**: Broadcom (on combo card RTL8273DE itself, works natively)
- **Ethernet**: Realtek RTL8168/8111
- **Card Reader**: Working

## ✅ Working

- Intel HD 620 with full graphics acceleration
- Brightness
- Audio (AppleALC + ALC236 layout)
- Sleep/Wake
- Battery status
- Synaptics trackpad (via VoodooSMBus)
- Internal keyboard and function keys
- USB ports
- Ethernet (Realtek RTL8111)
- Bluetooth (Broadcom card that is in my RTL8723DE, weirdly)
- Card reader
- Webcam

## 🚫 Not Working

- **WiFi**: Realtek 8723DE is not supported in macOS. Replace with a compatible 1x1 A+E Key card if you can find (couldnt find any compatible cards that match the criteria myself) or use a USB WiFi adapter.
- **HDMI**: No output, not functional at all.
- Anything else? Let me know!

## ⚠️ Notes

- Disable Secure Boot in BIOS.
- Generate your own serials with [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) before using.
- Tested with macOS Ventura & macOS Monterey. Adjust kexts if using an older OS version.
- Generate your own RTC-AWAC.aml SSDT using SSDTTime incase stuck in parsing error (Don't forget to patch after generating!)


## 💬 Credits

- OpenCore Team
- Dortania Guides: https://dortania.github.io/
- Acidanthera for all essential kexts
- CorpNewt for GenSMBIOS and ProperTree and many other essential tools



**Disclaimer:** Use this EFI at your own risk. Always keep backups of your data and BIOS settings.

Happy Hackintoshing! 🍏
