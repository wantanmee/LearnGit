2.4 Git Basics - Undoing Things
===
This is one of the few areas in Git where **you may lose some work** if you do it wrong.

## git-commit
If you want to try the previous commit again, you can run commit with the ```--amend``` option:
```bash
# it overwrites your previous commit
$ git commit -m 'initial commit'
$ git add forgotten_file
$ git commit --amend
```

## git-reset
Unstaging a staged file.
```bash
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

    renamed:    README.md -> README
    modified:   CONTRIBUTING.md
$ git reset HEAD CONTRIBUTING.md
Unstaged changes after reset:
M	CONTRIBUTING.md
    ```
> Actually ```git reset HEAD``` only reset the HEAD pointer, the file in your working directory is not touched

## git-checkout
Unmodifying a modified file.

It’s important to understand that ```git checkout -- [file]``` is a **dangerous** command. Any changes you made to that file are *gone*.
```bash
$ git status
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

    modified:   CONTRIBUTING.md
$ git checkout -- CONTRIBUTING.md
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

    renamed:    README.md -> README
```

---
> Usful Link: [Data Recovery](http://git-scm.com/book/en/v2/ch10/_data_recovery)

> Reference: http://git-scm.com/book/en/v2/Git-Basics-Undoing-Things
