2.5 Git Basics - Working with Remotes
===
## git-remote
To see which remote servers you have configured. 
```bash
$ git remote
origin
```
specify ```-v``` to show the URLs that Git has stored for the shortname to be used when reading and writing to that remote
```bash
$ git remote -v
bakkdoor  https://github.com/bakkdoor/grit (fetch)
bakkdoor  https://github.com/bakkdoor/grit (push)
cho45     https://github.com/cho45/grit (fetch)
cho45     https://github.com/cho45/grit (push)
defunkt   https://github.com/defunkt/grit (fetch)
defunkt   https://github.com/defunkt/grit (push)
koke      git://github.com/koke/grit.git (fetch)
koke      git://github.com/koke/grit.git (push)
origin    git@github.com:mojombo/grit.git (fetch)
origin    git@github.com:mojombo/grit.git (push)
```

To **add** a new remote Git repository as a shortname you can reference easily, run ```git remote add [shortname] [url]```:
```bash
$ git remote
origin
$ git remote add pb https://github.com/paulboone/ticgit
$ git remote -v
origin	https://github.com/schacon/ticgit (fetch)
origin	https://github.com/schacon/ticgit (push)
pb	https://github.com/paulboone/ticgit (fetch)
pb	https://github.com/paulboone/ticgit (push)
```
**Inspect** a remote

```git remote show [remote-name]```

**Remove** and **Rename** Remotes
```bash
$ git remote rename pb paul
$ git remote rm paul
```

## git-fetch
```git fetch [remote-name]``` command goes out to that remote project and pulls down *all the data* from that remote project that you don’t have yet. --  it *dosen't* merge or modify
```bash
$ git fetch pb
remote: Counting objects: 43, done.
remote: Compressing objects: 100% (36/36), done.
remote: Total 43 (delta 10), reused 31 (delta 5)
Unpacking objects: 100% (43/43), done.
From https://github.com/paulboone/ticgit
 * [new branch]      master     -> pb/master
 * [new branch]      ticgit     -> pb/ticgit
 ```
 
 ## git-push
 ```git push [remote-name] [local-branch-name]```
 
 ---
 > Reference: http://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes
