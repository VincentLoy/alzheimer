# Some CLI reminder

### Remove recursively all Apple's `.DS_Store` files *or whatever kind of files*

```console
$ find . -name '.DS_Store' -delete
```

### pip install saving in requirements.txt on the fly
```console
$ pip install [package] && pip freeze > /path/to/requirements.txt
```
