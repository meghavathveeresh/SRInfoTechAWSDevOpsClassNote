# SRInfoTechAWSDevOpsClassNote



29/04/2025::
=============

Introduction about the all tools 


<img width="846" alt="CI-CD" src="https://github.com/user-attachments/assets/1789ebfa-2809-465e-8dbc-01ad575eeba6" />



Integrate git & github::
==========================

![image](https://github.com/user-attachments/assets/85f36abd-f176-421c-8e44-4d56db4a057b)


What is Git?

Git is a free, open-source version control system (VCS) that helps developers manage their code. It's the most widely used tool VCS(version control system) Git is fast for committing, branching, merging, and comparing past versions Git is very high Performance and Flexibility,Security

Install Git in you local machine

https://git-scm.com/downloads/win

Please download the ---64-bit Git for Windows Setup.

Once download the git .exe file , double click and install the git on your machine

once installed right click on your local machine you can found Open Git batch here option, means git is installed successfully in your machine


![image](https://github.com/user-attachments/assets/e33acd91-3c58-4284-8e39-13f3f2b486d3)



GitHub account creation:: for creating github account EmailId is Required

go to link --https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home

Enter Email & password ,Username click continue ---Account will create successfully image


![image](https://github.com/user-attachments/assets/f0e311c5-629f-4e53-bf3a-3edee944eeff)



Github::Github is a one of the SCM(Source code management) tool and store the Project code.

Repository: storage area of your source code. Create a Repository on GitHub

click Repositories

Enter Repository Name::


![image](https://github.com/user-attachments/assets/a6d6c3c8-8814-45b3-8c39-994e6546470d)


Public:: Anyone on the internet can see this repository.

Private:: You choose who can see and commit to this repository.

Click Create Repository


![image](https://github.com/user-attachments/assets/c592782f-e429-43bb-a064-fbbe24d30c41)


Repository Created SUccessfully with Default branch main


![image](https://github.com/user-attachments/assets/bb4deaf9-ff56-473a-b3e6-46ac0346883e)



Github Introduction::
===============

GitHub is a web-based platform for version control and collaboration, allowing developers to store and manage their code in repositories.

Version Control: ::
GitHub uses Git, a distributed version control system, to track changes in code. This allows multiple people to work on the same project without overwriting each other's contributions.

Repositories::: where you can store your project files and track the history of changes made to those files.Public and private repos can be created depending on accessibility needs.


git commands::
================

git commands::

---git clone <github repository url>

>git clone https://github.com/srinfotech7358/AWSDevOps.git

>git status

>git add --all

>git commit -m "added some text files to Readmefile"

>git push

if we get any Access denied issues during push the changes from local to remote repository,please be authenticate below commands

>git config --global user.name "srinfotech7358"

>git config --global user.email "srinfotechbatch1@gmail.com"



Generate SSHKeys:: to Integarte Git to Github
==============================================

syntax::ssh-keygen -t ed25519 -C "your_email@example.com"


>ssh-keygen -t ed25519 -C "srinfotechbatch1@gmail.com"

Keys avaibale path and save the key (/c/Users/HP/.ssh/id_ed25519):

![image](https://github.com/user-attachments/assets/c1031abb-57bf-4585-88a9-e1fbb9358621)


![image](https://github.com/user-attachments/assets/ce78114d-1a3f-4adf-a677-c3f26736f6cc)


Please follow below links for more understanding 

https://docs.github.com/en/authentication/connecting-to-github-with-ssh

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

Once genearted the keys (public/private) and copy public key to Github Account

Go to -->settings


![image](https://github.com/user-attachments/assets/e6856f23-6d62-4e02-8fb2-05c720542ec3)



Click SSH and GPG Keys

![image](https://github.com/user-attachments/assets/906f1f68-79a8-4920-837f-38f165e5849e)


click New SSH Key

![image](https://github.com/user-attachments/assets/a461189f-f9e1-415c-b52e-c25f6cfaf1d2)


Add new SSH Key and click Add SSH Key


![image](https://github.com/user-attachments/assets/f62d4d90-f588-462b-bf04-54de51e566d8)




Lab Practice::
==============

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1

$ git clone git@github.com:srinfotech7358/AWSDevOps.git
Cloning into 'AWSDevOps'...
The authenticity of host 'github.com (20.207.73.82)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1

$ cd AWSDevOps/

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/AWSDevOps (main)

$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/AWSDevOps (main)

$ git add --all

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/AWSDevOps (main)
$ git commit -m "added some text to Readme.md file"
[main 95d0d52] added some text to Readme.md file
 1 file changed, 3 insertions(+), 1 deletion(-)

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/AWSDevOps (main)

$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Writing objects: 100% (3/3), 299 bytes | 149.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:srinfotech7358/AWSDevOps.git
   e38e1b1..95d0d52  main -> main

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/AWSDevOps (main)

$ git add --all

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/AWSDevOps (main)

$ git commit -m "added some text to Readme.md file"
[main 8ddd014] added some text to Readme.md file
 1 file changed, 3 insertions(+), 1 deletion(-)

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/AWSDevOps (main)

$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 311 bytes | 155.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:srinfotech7358/AWSDevOps.git
   95d0d52..8ddd014  main -> main



30/04/2025::
=============

Fork in Github::
====================

In GitHub, forking is a way to create your own copy of someone else's repository. example please fork below project to your own github account

https://github.com/srinfotech7358/spring-petclinic

steps to fork the project::
============================

Go to Above Project URL

https://github.com/srinfotech7358/spring-petclinic

![image](https://github.com/user-attachments/assets/5d3f74e8-b0f3-4875-a965-dea9aafe2ab8)

at top right we can found Fork option in github Account 

![image](https://github.com/user-attachments/assets/82f5b61e-cdc0-43f1-be3e-e335c1d236ce)

Click on Fork and click create Fork 

![image](https://github.com/user-attachments/assets/f115849b-aed6-4f6b-b72a-a62a86058c8b)

Successfully Fork done from someone else's repository 

once above steps done ,please clone the Project and Modified files and push to github repository


Lab Practice::
==================


HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1
$ git clone git@github.com:srinfotech7358/spring-petclinic.git
Cloning into 'spring-petclinic'...
remote: Enumerating objects: 10498, done.
remote: Total 10498 (delta 0), reused 0 (delta 0), pack-reused 10498 (from 1)
Receiving objects: 100% (10498/10498), 7.68 MiB | 941.00 KiB/s, done.
Resolving deltas: 100% (3964/3964), done.

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1
$ cd spring-petclinic/

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/spring-petclinic (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/spring-petclinic (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   pom.xml

no changes added to commit (use "git add" and/or "git commit -a")

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/spring-petclinic (main)
$ git add --all

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/spring-petclinic (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   pom.xml


HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/spring-petclinic (main)
$ git commit -m "modified pom.xml file"
[main f2ef175] modified pom.xml file
 1 file changed, 2 insertions(+)

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/spring-petclinic (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 325 bytes | 325.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:srinfotech7358/spring-petclinic.git
   0c88f91..f2ef175  main -> main

HP@DESKTOP-E518Q66 MINGW64 ~/Downloads/SR Infotech Batch1/spring-petclinic (main)
$
