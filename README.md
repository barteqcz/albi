# ALBI - Arch Linux Bash Installer

### About

ALBI aims to automate the Arch Linux installation process.

### Installing

```
pacman -Syy git
git clone https://github.com/barteqcz/albi
cd albi/
bash install
```
### Usage and preparation

Before running the script, it is necessary to manually, arbitrarily, but correctly partition the disk, and connect the device to the internet (**when it comes to wifi connection**). 
<br>
 
For help with partitioning, refer to https://wiki.archlinux.org/title/partitioning
<br>

For help with connecting the device to WIFI using `iwd`, refer to https://wiki.archlinux.org/title/iwd
<br>
 
To change locale settings, please edit 27 and 28 lines in `script` file accordingly. The default ones are set to English (United States).

### Troubleshooting

In case, you can't install `git` package because of keyring-related errors, do the following:

```
rm -rf /etc/pacman.d/gnupg/
killall gpg-agent
pacman-key --init
pacman-key --populate
pacman -Syy archlinux-keyring git
```
