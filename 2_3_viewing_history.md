# 2.3 Git Basics - Viewing the Commit History

## git-log
lists the commits made in that repository in *reverse* chronological order

```-p``` shows the difference introduced in each commit. You can also use ```-2```, which limits the output to only the last two entries:
```bash
$ git log -p -2
# abbreviated stats for each commit
$ git log --stat
```
```--pretty``` option changes the log output to formats other than the default. A few prebuilt options are available, such as ```oneline```, ```short```, ```full```, and ```fuller```
```bash
$ git log --pretty=oneline
```
```format``` option allows you to specify your own log output format.
```bash
$ git log --pretty=format:"%h - %an, %ar : %s"
ca82a6d - Scott Chacon, 6 years ago : changed the version number
085bb3b - Scott Chacon, 6 years ago : removed unnecessary test
a11bef0 - Scott Chacon, 6 years ago : first commit
```
```--graph``` option adds a nice little ASCII graph showing your branch and merge history
```bash
$ git log --pretty=format:"%h %s" --graph
```
```--grep``` only show commits with a commit message containing the string

```-S``` only show commits adding or removing code matching the string

> Detailed about git-log: http://git-scm.com/docs/git-log

> Reference: http://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History


