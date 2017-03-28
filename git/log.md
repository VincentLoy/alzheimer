# Git log

Tips about `$ git log`

## Improve git log rendering

Git log screen is really boring :(

![Boring logs](http://dl.dvp.io/gh/gitlog-boring.png)

But you can improve it easily!

![Pretty logs](http://dl.dvp.io/gh/gitlog-pretty.png)

```console
$ git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
```

The simpliest way to use this enhancement is to create an alias.

```console
$ git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```

If you want see the diff you can run `git lg -p`

![Diff logs](http://dl.dvp.io/gh/gitlog-diff.png)

