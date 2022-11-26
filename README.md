# ALBI - Arch Linux Bash Installer

### Installing

```
pacman -Syy git
git clone https://github.com/barteqcz/albi
cd albi/
bash install
```

### Troubleshooting

In case, you can't install `git` package because of some keyring-related errors, do the following:

```
pacman-key --init
pacman-key --populate
pacman -Syy archlinux-keyring git
```
