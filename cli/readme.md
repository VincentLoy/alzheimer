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

### find all files that end with newline
```console
$ find -type f -exec sh -c '[ -z "$(sed -n "\$p" "$1")" ]' _ {} \; -print
```

### find all files that doesn't end with newline
```console
$ find -type f -exec sh -c '[ -n "$(sed -n "\$p" "$1")" ]' _ {} \; -print
```
