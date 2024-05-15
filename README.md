# ironhack-lab1
Github repository for Git lab

`https://github.com/gustavoleonh/ironhack-lab1`

## #Task 1:

1. Trunk based:

	`git clone https://github.com/gustavoleonh/ironhack-lab1.git`
	 `Cloning into 'ironhack-lab1'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.`

`cd ironhack-lab1/`

`mkdir files`

`cd files/`

`nano file1.txt`

`git add file1.txt`

`git add  ../README.md`

`git commit -m "Fist commit"`

`git push origin main`

> Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 10 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 465 bytes | 465.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/gustavoleonh/ironhack-lab1.git
   3a74abd..2ddb18f  main -> main
   
   `nano file2.txt`
   
   `cd ..`
   
   `git add files/file2.txt`
   
   `git commit -m "Second commit"`
   
   `git push origin main`
   
>    Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 10 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 796 bytes | 796.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/gustavoleonh/ironhack-lab1.git
   2ddb18f..3a2e60d  main -> main
   
   `gst`
   
>    On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
	
2. Gitflow:

	`git branch develop`
	
	`git push origin develop`
	
> 	git push origin develop
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'develop' on GitHub by visiting:
remote:      https://github.com/gustavoleonh/ironhack-lab1/pull/new/develop
remote:
To https://github.com/gustavoleonh/ironhack-lab1.git
 * [new branch]      develop -> develop
	 
	 
	 `gst`
> 	 On branch develop
nothing to commit, working tree clean

`gco -b feature/dev-one`

`nano file1.txt`

`git add file1.txt`

`git commit -m "Feature one"`
> [feature/dev-one 81ae70d] Feature one
 1 file changed, 3 insertions(+)
 
 `git push origin feature/dev-one`
 
>  Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 10 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 392 bytes | 392.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'feature/dev-one' on GitHub by visiting:
remote:      https://github.com/gustavoleonh/ironhack-lab1/pull/new/feature/dev-one
remote:
To https://github.com/gustavoleonh/ironhack-lab1.git
 * [new branch]      feature/dev-one -> feature/dev-one

 `gco develop`
 
 `git merge feature/dev-one`
>  git merge feature/dev-one
Updating 1c146a1..81ae70d
Fast-forward
 files/file1.txt | 3 +++
 1 file changed, 3 insertions(+)
 
 `gco -b feature/dev-two`
 
 `nano file2.txt`
 
 `git add file2.txt`
 
 `git commit -m "Feature two"`
>  [feature/dev-two 2905b78] Feature two
 1 file changed, 2 insertions(+)
 
 `git push origin feature/dev-two`
>  Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 10 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 394 bytes | 394.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'feature/dev-two' on GitHub by visiting:
remote:      https://github.com/gustavoleonh/ironhack-lab1/pull/new/feature/dev-two
remote:
To https://github.com/gustavoleonh/ironhack-lab1.git
 * [new branch]      feature/dev-two -> feature/dev-two

 `gco develop`
 
 `git merge feature/dev-two`
>  Updating 81ae70d..2905b78
Fast-forward
 files/file2.txt | 2 ++
 1 file changed, 2 insertions(+)
 
 `gco main`
 
 `gco -b release`
 
 `git cherry-pick 81ae70d` -- In this case we just to release feature 1
 
 `gco main`
 
 `git merge release`
>  Updating 1c146a1..03e0cee
Fast-forward
 files/file1.txt | 3 +++
 1 file changed, 3 insertions(+)
 
 `cat file1.txt`
>  This is file 1
> Adding new feature

## #Task 2: Conflict Resolution and Merging

`git pull`
> remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), 1.03 KiB | 81.00 KiB/s, done.
From https://github.com/gustavoleonh/ironhack-lab1
   9d087ad..5b6635a  develop    -> origin/develop
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint:
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint:
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.

`git pull --rebase`

## #Task 3: Pull Request and Code Review Simulation

`gco main`

`gco -b feature/dev-pull-request`

`nvim file3.txt`

`git add file3.txt`

`git commit -m "Adding new file"`

`git push origin feature/dev-pull-request`

Pull request URL: https://github.com/gustavoleonh/ironhack-lab1/pull/1

![image](https://github.com/gustavoleonh/ironhack-lab1/assets/116121540/d4043bf0-ea35-4f77-a40a-b948564936f3)
