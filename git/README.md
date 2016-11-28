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

### Get titles of all commits for today
```console
git log --since=midnight --author="$(git config user.name)" --oneline
```

### Clean local merged branches
```console
git fetch -p && git branch --merged develop | grep -v 'master$' | grep -v 'develop$' | xargs git branch -d
```

### Get statuses of branches (xxx ahead, xxx behind) compared to origin
```console
git branch -v | grep -E 'ahead|behind' | sed -r 's/[ *]\s(\S*).*(\[(ahead|behind).+?\]).*/\1 \2/g'
```

### List all modified files in a speific commit
```console
git diff-tree --no-commit-id --name-only -r [COMMIT_SHA]
# or
git show --stat [COMMIT_SHA]
```

### List all modified files betwen two commits
```console
git diff --name-only SHA1 SHA2
```
