3.1 Git Branching - Branches in a Nutshell
===
A branch in Git is simply a lightweight movable **pointer** to one of the commits.

## git-branch

* Create branch

    ```Shell
# this command only create a new branch, not switch to that branch
$ git branch testing
    ```
* Switch branches

    ```Shell
$ git checkout testing
    ```
    
Running ```git log``` with ```--decorate``` option to see where the branch pointers are pointing.
```Shell
$ git log --oneline --decorate
f30ab (HEAD, master, testing) add feature #32 - ability to add new
34ac2 fixed bug #1328 - stack overflow under certain conditions
98ca9 initial commit of my project
```
To print out the history of your commits, showing where your branch pointers are and how your history has diverged:
```Shell
$ git log --oneline --decorate --graph --all
* c2b9e (HEAD, master) made other changes
| * 87ab2 (testing) made a change
|/
* f30ab add feature #32 - ability to add new formats to the
* 34ac2 fixed bug #1328 - stack overflow under certain conditions
* 98ca9 initial commit of my project
```

---
> http://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell
