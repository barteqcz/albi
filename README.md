# ALBI - Arch Linux Bash Installer

### Installing

```
pacman -Syy git
git clone https://github.com/barteqcz/albi
cd albi/
bash install
```
### Usage and preparation

Before running the script, it is necessary to manually, arbitrarily, but correctly partition the disk, and connect the device to the internet (when it comes to wifi connection). To do that, you can use `iwd` <br>
For help with partitioning, please refer to https://wiki.archlinux.org/title/partitioning <br>
For help with connecting the device to WIFI using `iwd`, please refer to https://wiki.archlinux.org/title/iwd

### Troubleshooting

In case, you can't install `git` package because of some keyring-related errors, do the following:

```
rm -rf /etc/pacman.d/gnupg/
killall gpg-agent
pacman-key --init
pacman-key --populate
pacman -Syy archlinux-keyring git
```
