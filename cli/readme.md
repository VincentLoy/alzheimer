# Some CLI reminder

### Remove recursively all Apple's `.DS_Store` files *or whatever kind of files*

```console
$ find . -name '.DS_Store' -delete
```

### Remove recursively all `node_modules` folder (or any folders you want). Saves a lot of space.

```console
$ find . -name "node_modules" -exec rm -rf '{}' +
```

### Resize all images of a certain format by a certain percentage (e.g png, 50%)

```console
$ for i in *.png; do convert $i -resize 50% $i;done
```

### Zip a folder
```console
$ zip -r foo.zip dir_path
```

### Find all files that end with newline
```console
$ find -type f -exec sh -c '[ -z "$(sed -n "\$p" "$1")" ]' _ {} \; -print
```

### Find all files that doesn't end with newline
```console
$ find -type f -exec sh -c '[ -n "$(sed -n "\$p" "$1")" ]' _ {} \; -print
```

### How to kill a process running on particular port in Linux
example with port `8080` - seen [here](http://stackoverflow.com/questions/11583562/how-to-kill-a-process-running-on-particular-port-in-linux).

list any process listening to the port 8080
```console
lsof -i:8080
```

Kill any process on port 8080
```console
kill $(lsof -t -i:8080)
```

More violent way to do it
```console
kill -9 $(lsof -t -i:8080)
```

### Set the date to current time in FreeBSD (if current date is too shifted for NTP)

```console
date -f '%a, %d %b %Y %T %Z' "`curl -s -k -I 'https://www.ovh.com/fr' | grep -Fi 'Date:' | sed 's/Date: //'`"
```

### Config a folder for www-data editable by user (for local dev stuff)
```console
sudo chown www-data /path/to/the/folder -Rf 
sudo chmod 775 -R /path/to/the/folder
```
