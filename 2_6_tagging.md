2.6 Git Basics - Tagging
===
## git-tag
- list tags
	```bash
 $ git tag
 v0.1
 v1.3
	```
	list particular tags:
	```bash
 $ git tag -l 'v1.8.5*'
 v1.8.5
 v1.8.5-rc0
 v1.8.5-rc1
 v1.8.5-rc2
 v1.8.5-rc3
	```
- create tags
    - annotated: stored as full objects in the Git database. Specify ```-a``` to created annotated tag. To tag a *history* commit, specify the commit checksum (or part of it) at the end of the command:
    	```bash
    $ git tag -a v1.4 -m 'my version 1.4'
    $ git tag -a v1.2 9fceb02
    	```
    - lightweight tag:  a pointer to a specific commic, nomarlly for *temporary* tag.
    	```bash
    $ git tag v1.4-lw
    	```
- show tag inforamtion
	```bash
$ git show v1.4
	```
- share tags  
	By default, the git push command doesn’t transfer tags to remote servers. You will have to explicitly push tags to a shared server with ```git push origin [tagname]```.    
	```
 $ git push origin --tags
 Counting objects: 1, done.
 Writing objects: 100% (1/1), 160 bytes | 0 bytes/s, done.
 Total 1 (delta 0), reused 0 (delta 0)
 To git@github.com:schacon/simplegit.git
 * [new tag]         v1.4 -> v1.4
 * [new tag]         v1.4-lw -> v1.4-lw
 	```
 
- check out tags  
 If you want to put a version of your repository in your working directory that looks like a specific tag, you can create a new branch at a specific tag with git checkout ```-b [branchname] [tagname]```

---
> Reference: http://git-scm.com/book/en/v2/Git-Basics-Tagging
