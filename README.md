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
	
2. Gitflow:
	 