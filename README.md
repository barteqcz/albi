<b> ALBI - Arch Linux Bash Installer <b/>

```
pacman -Syy git
git clone https://github.com/barteqcz/albi
cd albi/
bash install
```
CURRENTLY IN ALPHA VERSION (THE SCRIPT IS INCOMPLETE), DON'T RUN IT ON REAL HARDWARE

<b> Troubleshooting <b/>

In case, you can't install `git` package because of some keyring-related errors, do the following:

```
pacman-key --init
pacman-key --populate
pacman -Syy archlinux git
```
