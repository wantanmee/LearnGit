3.3 Git Branching - Branch Management
===
List branch:
```Bash
$ git branch
  iss53
* master
  testing
```
Use ```-v``` option to see the last commit on each branch
```Bash
$ git branch -v
  iss53   93b412c fix javascript issue
* master  7a98805 Merge branch 'iss53'
  testing 782fd34 add scott to the author list in the readmes
```
```--merged``` and ```--no-merged``` options can filter this list to branches that you have or have not yet merged into the branch you’re currently on.
```Bash
$ git branch --no-merged
  testing
```
----
> Reference: http://git-scm.com/book/en/v2/Git-Branching-Branch-Management
    
