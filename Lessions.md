First clone the remote repository (demo-repo)
LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo
$ git clone https://github.com/SagarPattnaik/demo-repo.git
LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo
$ cd demo-repo/
LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ ls -la
total 5
drwxr-xr-x 1 LENOVO 197121  0 May 30 23:18 ./
drwxr-xr-x 1 LENOVO 197121  0 May 30 23:18 ../
drwxr-xr-x 1 LENOVO 197121  0 May 30 23:20 .git/
-rw-r--r-- 1 LENOVO 197121 29 May 30 23:18 README.md

Modify README.md
Add index.html

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

no changes added to commit (use "git add" and/or "git commit -a")

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git add .

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   index.html

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git commit -m "Added Index.html" -m "Initial Commit"
[main 268e064] Added Index.html
 2 files changed, 5 insertions(+)
 create mode 100644 index.html


LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ ssh-keygen -t rsa -b 4096 -C "sagarpattnaik60@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/LENOVO/.ssh/id_rsa): testkey
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in testkey
Your public key has been saved in testkey.pub
The key fingerprint is:
SHA256:O3NgGUmarHXBEwWeA0fiWXn4NtxaMqGAW9HwXKsGZ7g sagarpattnaik60@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
|     .=*O*o      |
|    .oo#*=o.     |
|     oX.%*.o     |
|    .o *.=B o    |
|    . E S. *     |
|       o o.      |
|        + .      |
|         +       |
|                 |
+----[SHA256]-----+

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ ls | grep testkey
testkey
testkey.pub

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ cat testkey.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQDnY74FQ4ukhA0NjDE48DJ79qDTBRNDQbEOw5m4ix0b1AVslHgnkd+yjKCHuoIsBl6S8aEI11Oi8f4QGBVrhE9Yj94pnywgUrbcW/pFenqCAQqOhXR0KEfDUq9XuDrOfLlsUtkzelhDr5KegZo6eiMVs/7vyJJGm7AKG3diK3h38Y2woxQDWuQrJi7bX7m7qGElOBU5EOXowiNY6MPuY7NouRaNUQ3rdz4Xl8JGcrfU1BlxuYROG7FHg91U/gg4+6EetI2XNKFhn2XK7iFcLFiq+Fbri2d1YDZdi+hN5oNBUyz0Ut51x+nou2QI3eBPgqU+WTi7k/euuTBuDNqsa028IXqkoBPZX+rMxtct3unKaWLO8YxS82kkQTICmcQMjhsk3a9qXdSfd+u+HjDmXVbxNEHj4myKBX51bMSs8iTkls+SI9rDib8CP7rSzTakCjp1c1qZstD9kLb/V/F69TPOftdOvnTAZyaw/XxmGug3jaaqLlFQW081ddoRc9a0THn1IHKxy8pct57gDRD2FuNbOh+cRrU50qDdya2bd6VpHGebyQUB1guBLO5NdwARNmTDUaSJF/hwcS79WkrBQJ8CQC9xoRnHJU/Hn8x5qO6+bVSR3BWDaChmZchReEd4qREvv0jA4RRrgjiRGJKe6WmX0qB8OAe2+nxLB+UB/0H43Q== sagarpattnaik60@gmail.com
LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ ssh-add testkey
Identity added: testkey (sagarpattnaik60@gmail.com)
LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git add .
LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   testkey
        new file:   testkey.pub
LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (8/8), 3.27 KiB | 3.27 MiB/s, done.
Total 8 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/SagarPattnaik/demo-repo.git
   afe59d8..e27055c  main -> main
branch 'main' set up to track 'origin/main'.

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git push origin main
Everything up-to-date

Creating a new repository in local folder and push it to github

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo
$ cd demo-repo2/

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2
$ ls -la
total 0
drwxr-xr-x 1 LENOVO 197121 0 May 31 11:03 ./
drwxr-xr-x 1 LENOVO 197121 0 May 31 11:03 ../

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 
$ git init
Initialized empty Git repository in C:/Sagar/Repo/GitHub/Demo/demo-repo2/.git/

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)
$ ls -la
total 5
drwxr-xr-x 1 LENOVO 197121  0 May 31 11:06 ./drwxr-xr-x 1 LENOVO 197121  0 May 31 11:03 ../
drwxr-xr-x 1 LENOVO 197121  0 May 31 11:06 .git/
-rw-r--r-- 1 LENOVO 197121 21 May 31 11:05 README.md

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)    
        README.md

nothing added to commit but untracked files present (use "git add" to track)

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)
$ git add .

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md


LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)
$ git commit -m "Created README" -m "description"
[master (root-commit) a4a33fc] Created README
 1 file changed, 3 insertions(+)
 create mode 100644 README.md

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)
$ git remote add origin https://github.com/SagarPattnaik/demo-repo2.git

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)
$ git remote -v
origin  https://github.com/SagarPattnaik/demo-repo2.git (fetch)
origin  https://github.com/SagarPattnaik/demo-repo2.git (push)

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)
$ git push -u origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 251 bytes | 31.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/SagarPattnaik/demo-repo2.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo2 (master)

Git Branches;

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo
$ cd demo-repo

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ pwd
/c/Sagar/Repo/GitHub/Demo/demo-repo

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git branch
* main

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git checkout -b feature-1
Switched to a new branch 'feature-1'

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (feature-1)
$ git branch
* feature-1
  main

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (feature-1)
$ git checkout main
Switched to branch 'main'
M       Lessions.md
Your branch is up to date with 'origin/main'.       

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git branch
  feature-1
* main

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git checkout feature-1
Switched to branch 'feature-1'
M       Lessions.md

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (feature-1)
$ git status
On branch feature-1
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Lessions.md
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (feature-1)

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (feature-1)
$ git add .

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (feature-1)
$ git status
On branch feature-1
Changes to be committed:
  (use "git restore --staged <file>..." to unstage) 
        modified:   Lessions.md
        modified:   README.md


LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (feature-1)
$ git commit -m "updated readme and lessions file"  
[feature-1 04b68ae] updated readme and lessions file
 2 files changed, 132 insertions(+), 2 deletions(-) 

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (feature-1)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.       

LENOVO@DESKTOP-MU2L3BP MINGW64 /c/Sagar/Repo/GitHub/Demo/demo-repo (main)
$ git checkout feature-1 
Switched to branch 'feature-1'