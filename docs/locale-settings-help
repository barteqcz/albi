# Manual for setting locale

### Setting locale in /etc/locale.conf

It's done by echoing `LANG=en_US.UTF-8` to `/etc/locale.conf`
To set your desired locale setting, you have to replace, `en_US` with appropiate locale setting. It's recommended to use UTF-8 encoding though. List of available entries, is there:

There will be the list

### Setting locale in /etc/locale.gen

It's done by uncommenting appropiate line in `/etc/locale.gen` file. In ALBI, it's done with the help of `sed` command.
```
sed -i '/en_US.UTF-8/s/^#//g' /etc/locale.gen
```
In this case, you have to replace `en_US` with appropiate locale setting. Again, it's recommended to use UTF-8 encoding. List of available entries is available in `locale.gen` file, and here is what it looks like:

There will be the list
