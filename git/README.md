## Some Git command to save your life


### Remove files or folders from Git without deleting them
```console
$ git rm --cached mylogfile.log
$ git rm --cached -r mydirectory
```

### Delete a tag localy
```console
git tag -d [TAG_NAME]
```

### Delete an already pushed tag
```console
git push origin :refs/tags/[TAG_NAME]
```
