# ALBI - Arch Linux Bash Installer

### Installing

```
curl https://github.com/barteqcz/albi
cd albi/
bash install
```

### Configuration

There are some elements, that you should configure in a detached file - `config.conf`

### Troubleshooting

In case, you can't install `git` package because of some keyring-related errors, do the following:

```
rm -rf /etc/pacman.d/gnupg/
killall gpg-agent
pacman-key --init
pacman-key --populate
pacman -Syy archlinux-keyring git
```
