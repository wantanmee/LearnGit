2.2 Git Basics - Recording Changes to the Repository
====
![Life Cycle](http://git-scm.com/book/en/v2/book/02-git-basics/images/lifecycle.png  "The lifecycle of the status of your files.")

## git-status
   
    $ git status
    On branch master
    nothing to commit, working directory clean

get a far more simplified output from the command:

    $ git status -s
    
## git-diff
diff with no other arguments compares what is in your *working* directory with what is in your *staging area*
```bash
$ git diff
```
```--staged``` arguments compares your staged changes to your last commit.
```bash
# --staged and --cached are synonyms
$ git diff --staged
```    
## git-add
The git add command takes a path name for either a *file* or a *directory*; if it’s a directory, the command adds all the files in that directory recursively.

git add is a **multipurpose** command – you use it to begin tracking *new* files, to *stage* files, and to do other things like marking merge-conflicted files as resolved. It may be helpful to think of it more as **“add this content to the next commit”** rather than “add this file to the project”.

Git stages a file **exactly** as it is when you run the git add command.

## git-commit
    $ git commit
you can pass the ```-v``` option to git commit. Doing so also puts the diff of your change in the editor as well as the status
```bash
# Alternatively, you can type your commit message inline
$ git commit -m "Story 182: Fix benchmarks for speed"
```    
Adding the ```-a``` option to the git commit command makes Git automatically stage every file that is already tracked before doing the commit, letting you skip the *git add* part
```bash
$ git commit -a -m 'added new benchmarks'
```   
## git-rm
remove file from your *staging area*
```bash
$ git rm PROJECTS.md
```    
use the ```--cached``` option to keep the file on your hard drive but not have Git track it:
```bash
$ git rm --cached README
```    
You can pass files, directories, and file-glob patterns to the git rm command:
```bash
# Note the backslash (\) in front of the *. 
# This is necessary because Git does its own filename expansion in addition to your shell’s filename expansion.
# This command removes all files that have the .log extension in the log/ directory.
$ git rm log/\*.log
# This command removes all files that end with ~:
$ git rm \*~
```

## git-mv
If you want to rename a file in Git, you can use ```mv``` command:
```bash
$ git mv file_from file_to
```
## .gitignore
Setting up a .gitignore file before you get going is generally a good idea so you don’t accidentally commit files that you really don’t want in your Git repository.

The rules for the patterns you can put in the .gitignore file are as follows:
* Blank lines or lines starting with # are ignored.
* Standard glob patterns work.
* You can end patterns with a forward slash (/) to specify a directory.
* You can negate a pattern by starting it with an exclamation point (!).

> Useful example: https://github.com/github/gitignore

---

> Reference: http://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository
