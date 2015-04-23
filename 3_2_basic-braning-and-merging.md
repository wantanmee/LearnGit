3.2 Git Branching - Basic Branching and Merging
===
* Create and switch to a branch

    ```bash
$ git checkout -b iss53
    ```
    
* Merge branch
    ```bash
# first check out the branch you wish to merge into
$ git checkout master
$ git merge hotfix
    ```
> with ```--no-ff``` option will disable *fast forward* in that merge opration, and the merge will create a commit log.     
* Delete branch
    ```bash
$ git branch -d hotfix
    ```
    
---
> Reference: http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging
