# Some CLI reminder

### Remove recursively all Apple's `.DS_Store` files *or whatever kind of files*

```console
$ find . -name '.DS_Store' -delete
```

### Resize all images of a certain format by a certain percentage (e.g png, 50%)

```console
$ for i in *.png; do convert $i -resize 50% $i;done
```

### Zip a folder
```console
$ zip -r foo.zip dir_path
```
