Fork from https://git.mauras.ch/voidlinux/luks-lvm-install
Additional credit to https://www.daveeddy.com/2018/09/05/encrypted-void-linux-install-on-my-thinkpad-x1-carbon/

Voidlinux LUKS + LVM installer
------------------------------

Basic install script that replaces completely the standard VoidLinux installer.  

### Features

- Full Disk Encryption for both `boot` and `root` partitions
- Detects UEFI mode and creates partitions accordingly
- Set options from a config file
- Let's you define your LVs from config file
- Supports execution of custom scripts inside install chroot for easy customization
- Optionally add swap

### Usage

- Boot a VoidLinux LiveCD
- Setup your network
- Install Git `xbps-install -S git`

Then:

```
git clone http://git.mauras.ch/voidlinux/https://github.com/egyb2h9/voidlinux-luks-lvm-install.git
cd voidlinux-luks-lvm-install
```
Edit `config` to your taste.  
If needed put your `.sh` scripts in custom dir - see examples - before running `install.sh`  
```
./install.sh
```
