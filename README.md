# Proxmox-VE install from iso support
Directly install Proxmox-VE from Official Proxmox-VE Installation Media using grub2 without burning to usb-drive.

# Features
- Filesystems: ext4, exfat 
- Provide boot menu
- Supported ISOs: Proxmox-VE-x86_64 of 2026 (9.2-1 tested).

# Usage
Load provided 'proxmox921.img' file along with the main 'initrd' of the installation media via grub loopback module.
If you are using 'https://github.com/Mexit/MultiOS-USB', it is just a few steps:

0. Use MultiOS-USB partition on 'ext4' or 'exfat' filesystem.
1. Copy your Proxmox-iso files to 'ISOs' directory.
2. Create a directory for 'grub.cfg' files: '/MultiOS-USB/config_priv/proxmox-sc'
3. Copy 'proxmox921.img', 'proxmox-ve-9.2-1-installer.cfg' over there.
4. Reboot into 'MultiOS-USB' and start e.g. 'proxmox-ve_9.2-1.iso [scandev]' entry.
5. Installer will start same way as from usb-stick.
