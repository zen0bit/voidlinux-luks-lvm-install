Fork from https://github.com/egyb2h9/voidlinux-luks-lvm-install
which was Forked from https://git.mauras.ch/voidlinux/luks-lvm-install
Additional credit to 
- https://www.daveeddy.com/2018/09/05/encrypted-void-linux-install-on-my-thinkpad-x1-carbon/
- https://www.daveeddy.com/2018/09/15/using-void-linux-as-my-daily-driver/
- https://alkusin.net/voidlinux/

Voidlinux LUKS + LVM installer
------------------------------

Basic install script that replaces the standard VoidLinux installer.  

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
```
# wpa_passphrase 'ssid' >> /etc/wpa_supplicant/wpa_supplicant.conf
password<enter>
# sv restart dhcpcd
```
- Install wget `xbps-install -S wget`

Then:

```
wget https://raw.githubusercontent.com/foodotooo/voidlinux-luks-lvm-install/master/install.sh
chmod +x install.sh
./install.sh
```
