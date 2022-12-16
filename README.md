# ALBI - Arch Linux Bash Installer

### About

ALBI aims to automate the Arch Linux installation process.

### Installing

```
pacman -Sy git
git clone https://github.com/barteqcz/albi
cd albi/
bash install
```
### Usage and preparation

Before running the script, it is necessary to manually, arbitrarily, but correctly partition the disk, and connect the device to the internet (**when it comes to wifi connection**). 
<br>
 
For help with partitioning, refer to https://wiki.archlinux.org/title/partitioning#Example_layouts
<br>

For help with connecting the device to WIFI using `iwd`, refer to https://wiki.archlinux.org/title/iwd
<br>
 
To see list of available locales, see [this](https://github.com/barteqcz/albi/blob/main/docs/locales.md)

### Troubleshooting

In case, you can't install `git` package because of keyring-related errors, do the following:

```
rm -rf /etc/pacman.d/gnupg/
killall gpg-agent
pacman-key --init
pacman-key --populate
pacman -Sy archlinux-keyring git
```
### Post-install

<b> Dualbooting </b>

In case you're dualbooting Arch with, for example, Windows, after the installation, you'll have to run
```
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
to let `GRUB` recreate the config file and automatically detect, for example, the Windows OS.

<b> Setting the system regional setting </b>

To enable specific locales settings, you have to edit `/etc/locale.gen` and uncomment desired ones. <br>
To edit the file you can use `vim`, `nano`, or some graphical editors, but remember to run it as superuser, to edit that file. <br>
If you already uncommented your desired locales, run
```
sudo locale-gen
```
