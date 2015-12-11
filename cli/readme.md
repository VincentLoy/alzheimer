# Some CLI reminder

### Remove recursively all Apple's `.DS_Store` files *or whatever kind of files*

```console
$ find . -name ".DS_Store" -print0 | xargs -0 rm -rf
```
