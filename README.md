# OpenCore-EFI-for-NUC8i7HVK
Bootable OC EFI that Functional with macOS Sequoia and Tahoe

# Usage for macOS 15 Sequoia
1. Rename Config-Sequoia.plist to Config.plist
2. Run macOS installer until finish
3. After installing, using tools like OCAT to generate your SMBIOS
4. Using OCLP-Mod for intel wireless fixing

# Usage for macOS 26 Tahoe
1. Rename Config-Tahoe-Installer.plist to Config.plist
2. Run macOS installer until finish and make sure FileVault is disabled
3. After installing, Rename Config-Tahoe.plist to Config.plist
4. using tools like OCAT to generate your SMBIOS
5. if FileVault is accidentally enabled, switch to Config-Tahoe-FileVault.plist, disable FileVault, and switch it back
6. Using OCLP-Mod for audio fixing

# Issues
***AirportItlwm*** can't function in macOS 26 Tahoe

# Notes
### Config-Sequoia
* All perfect for Sequoia, using ***AirportItlwm*** for wireless
### Config-Tahoe
* Mostly good for Tahoe, using ***Itlwm*** for wireless, need modifying SSID and password in Info.plist in Itlwm.kext for Wi-Fi Connection
### Config-Tahoe-Installer
* Disable ***WhatEverGreen*** for installing macOS 26 Tahoe
* Disable ***UEFI-APFS-EnableJumpStart*** for FileVault support
* Enable ***apfs_aligned.efi*** in UEFI-Drivers for FileVault support
### Config-Tahoe-FileVault
* Disable ***UEFI-APFS-EnableJumpStart*** for FileVault support
* Enable ***apfs_aligned.efi*** in UEFI-Drivers for FileVault support
