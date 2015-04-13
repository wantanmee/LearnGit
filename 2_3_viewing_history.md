# 2.3 Git Basics - Viewing the Commit History

## git-log
lists the commits made in that repository in *reverse* chronological order

```-p``` shows the difference introduced in each commit. You can also use ```-2```, which limits the output to only the last two entries:
```git
# testing
$ git log -p -2
```
