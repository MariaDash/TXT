# TXT_GIT_Homework_1
## 1. Create an external repository called XML_GIT on Github site.
I go to https://github.com/MariaDash, click "Repositories", click "New", make it Public, add README.md file, create repository.
## 2. Clone repository to local PC
I go to repository page--> Code --> Local and copy its link. And here two options: 
You can copy by HTTPS (unsecure without password) or SSH (need specific configuration and it is secure and always ask password).. I cpoy via HTTPS.
On PC I go to my folder "GIT", right click "Gitbash Here" and open a terminal Gitbash in this folder.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git (main)
$ git clone https://github.com/MariaDash/TXT.git
Cloning into 'TXT'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git (main)
$cd TXT
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ ls 
README.md
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$
```
Note: if you need to change your working repository:
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$git remote set-url origin https://github.com/MariaDash/TXT.git
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git remote -v
origin  https://github.com/MariaDash/TXT.git (fetch)
origin  https://github.com/MariaDash/TXT.git (push)
```

## 3. Inside the local TXT, create a “new.txt” file.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ echo > new.txt

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ ls
README.md  new.txt
```
## 4. Track the file new.txt
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        new.txt

nothing added to commit but untracked files present (use "git add" to track)

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git add new.txt
warning: in the working copy of 'new.txt', LF will be replaced by CRLF the next time Git touches it

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   new.txt

```
## 5. Commit the file new.txt
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git commit -m "creation of new.txt"
[main 7d49728] creation of new.txt
 1 file changed, 1 insertion(+)
 create mode 100644 new.txt

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ 
```
## 6. Send the file new.txt to the remote repository
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 278 bytes | 278.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MariaDash/TXT.git
   cbe0218..7d49728  main -> main

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$
```
## 7. Edit the contents of the “new.txt” file - write information about yourself (full name, age, number of pets, future desired salary). Everything should be written in TXT format.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ vim new.txt

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ cat new.txt
info:
Mariia
Dashkova
Age 35
Pets 0
Salary $1500

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$
```
## 8. Send changes to remote repository.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   new.txt

no changes added to commit (use "git add" and/or "git commit -a")

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git commit -am "update new.xml"
warning: in the working copy of 'new.txt', LF will be replaced by CRLF the next time Git touches it
[main 16f08bb] update new.xml
 1 file changed, 6 insertions(+), 1 deletion(-)

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 326 bytes | 326.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/MariaDash/TXT.git
   7d49728..16f08bb  main -> main

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$
```
## 9. Create preferences.txt file
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ vim preferences.txt

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ 
```
## 10. Add information about your preferences (Favorite movie, favorite series, favorite food, favorite season, side you would like to visit) in the file preferences.txt in TXT format.
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ cat preferences.txt
Preferences:
favourite movie: "G. I. Jane"
favourite tv show: "Friends"
favourite food: pizza
favourite season: winter
country to travel: Italy

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$
```
## 11. Create a file skills.txt add information about the skills that will be studied on the course in TXT format
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ vim skills.txt

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$
```
## 12. Do one string commit
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git add . && git commit -m "add and commit changes in preferences.txt and skills.txt"
warning: in the working copy of 'preferences.txt', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'skills.txt', LF will be replaced by CRLF the next time Git touches it
[main bac91f9] add and commit changes in preferences.txt and skills.txt
 2 files changed, 14 insertions(+)
 create mode 100644 preferences.txt
 create mode 100644 skills.txt

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$
```
## 13. Send at once two files to the remote repository
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git push
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 837 bytes | 418.00 KiB/s, done.
Total 6 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/MariaDash/TXT.git
   c81b72a..f4ece71  main -> main

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$
```
## 14. Create a bug_report.txt file on the web interface.
## 15. Make Commit changes (save) changes on the web interface.
## 16. Modify the bug_report.txt file on the web interface, add a bug report in TXT format.
## 17. Make Commit changes (save) changes on the web interface.
## 18. Synchronize external and local TXT repository
```
Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$ git pull
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 2), reused 1 (delta 0), pack-reused 0
Unpacking objects: 100% (6/6), 1.25 KiB | 98.00 KiB/s, done.
From https://github.com/MariaDash/TXT
   f4ece71..e7f8f11  main       -> origin/main
Updating f4ece71..e7f8f11
Fast-forward
 bug_report.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 bug_report.txt

Admin@DESKTOP-V6V9F0T MINGW64 /d/Testing_Course/Git/TXT (main)
$
```
