

# SRInfoTechAWSDevOpsClassNote



29/04/2025::
=============


Introduction about the all tools 


![image](https://github.com/user-attachments/assets/142f944d-7d16-4c34-b8ee-d4da6e779449)





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



01/05/2025::
=============


Github branching strategy::
===========================


<img width="846" alt="Untitled" src="https://github.com/user-attachments/assets/406f212d-86de-4283-99f7-f8f823c99baf" />



![image](https://github.com/user-attachments/assets/d3e48811-53a0-4a2a-af7d-3044ecaefecc)



A GitHub branching strategy is crucial for maintaining an organized workflow in version control. There are different strategies depending on the size of the project, the number of team members, and the desired workflow. Here are some common branching strategies used in GitHub:

main or master branch:: This is default branch and whenever we created the empty Repository by defauly main or master branche is created automatically.
main or master branch always stable and live code 

feature branch:: It could be a new feature, an improvement of existing features, bug fixes, or any other changes. A feature branch is a type of branch in Git typically used to develop new features for the software.feature branch will created from main or master OR feature branch created from latest release branch always based on the release cycle

formate:: feature/YYYY.MM.DD
 feature/2025.03.17

release branch:: Based on the release we have created release branch accourdingly and starts the next release cycle.
always release branch created from master only and master have stable and live code and post release we shold merged code changes to master branch only

release/2025.03.17

hotfix branch:: always created from main or master branch only for production fixes.once production fix done we should merged directly to main or master branch only.

always created this hotfix branch for production issues fixes

bugfix:: this branch is created from release branch to fix the LLE(lower level environemnt)/Pre-Prod/UAT/Non-Prod issues and once LLE issues fixed ,we should pushed their changes to release branch only.

cloning references::

![image](https://github.com/user-attachments/assets/87f6ed4a-095b-4faa-854a-7fcdc019f31f)


Generate SSHKeys::

syntax::ssh-keygen -t ed25519 -C "your_email@example.com"

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

Clone Project code using SSH URL::
===============================

>git clone git@github.com:ifocusbatch2/spring-petclinic.git

![image](https://github.com/user-attachments/assets/1b704706-cfe5-4db1-8917-e7ca4c44e35f)

![image](https://github.com/user-attachments/assets/12f6150b-e9e9-4615-9864-4e3424a594dd)

![image](https://github.com/user-attachments/assets/03037e55-f77d-499e-b845-4e775b82afed)

![image](https://github.com/user-attachments/assets/8c5653a0-1427-4b26-968b-cda90c04cc48)


Lab Practice::
==============

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17
$ git clone git@github.com:ifocusbatch2/spring-petclinic.git
Cloning into 'spring-petclinic'...
The authenticity of host 'github.com (20.207.73.82)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
remote: Enumerating objects: 10430, done.
remote: Total 10430 (delta 0), reused 0 (delta 0), pack-reused 10430 (from 1)
Receiving objects: 100% (10430/10430), 7.67 MiB | 1.17 MiB/s, done.
Resolving deltas: 100% (3935/3935), done.

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17
$ cd spring-petclinic/

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   pom.xml

no changes added to commit (use "git add" and/or "git commit -a")

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (main)
$ git add --all

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (main)
$ git commit -m "updated pom.xml file"
[main b2e46bf] updated pom.xml file
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 340 bytes | 340.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:ifocusbatch2/spring-petclinic.git
   2aa53f9..b2e46bf  main -> main

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (main)
$ git checkout -b feature/2025.03.17
Switched to a new branch 'feature/2025.03.17'

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (feature/2025.03.17)
$ git status
On branch feature/2025.03.17
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   pom.xml

no changes added to commit (use "git add" and/or "git commit -a")

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (feature/2025.03.17)
$ git add --all

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (feature/2025.03.17)
$ git status
On branch feature/2025.03.17
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   pom.xml


HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (feature/2025.03.17)
$ git commit -m "added branch"
[feature/2025.03.17 f393310] added branch
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (feature/2025.03.17)
$ git push
fatal: The current branch feature/2025.03.17 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin feature/2025.03.17

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


HP@DESKTOP-E518Q66 MINGW64 ~/Desktop/Ifocus/batch2_17/spring-petclinic (feature/2025.03.17)
$ git push origin feature/2025.03.17
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 302 bytes | 302.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'feature/2025.03.17' on GitHub by visiting:
remote:      https://github.com/ifocusbatch2/spring-petclinic/pull/new/feature/2025.03.17
remote:
To github.com:ifocusbatch2/spring-petclinic.git
 * [new branch]      feature/2025.03.17 -> feature/2025.03.17





Raise PR (Pull Request) :: 
=================================

Merge the code from one branch to another branch that is called pull request

below are the steps to raise PR::

Go to -->Pull requests and click

![image](https://github.com/user-attachments/assets/5cfe4883-dd46-4643-a506-b54262c36202)

Click New Pull Request::

![image](https://github.com/user-attachments/assets/37020743-a2e9-4163-9afd-7680d58fc63a)

![image](https://github.com/user-attachments/assets/dad8eec2-b480-460f-8715-9d9c5fc3c12d)

please select base & compare branches so here base branch is release/2025.02.25 and compare branch is feature/2025.02.25

i'm going to merge code changes from feature branch to release branch 

![image](https://github.com/user-attachments/assets/185f0572-c51a-4ab2-884c-d2694522b268)

click create pull request

![image](https://github.com/user-attachments/assets/91068166-9d06-4b47-9d68-8c1251b0872f)

![image](https://github.com/user-attachments/assets/08a98671-c810-46fc-9024-17bae7538a61)


parasa7358 wants to merge 1 commit into release/2025.02.25 from feature/2025.02.25  

click merge request

![image](https://github.com/user-attachments/assets/44a4b84e-1aef-4b19-a93e-64e48b362b29)


confirm merge

![image](https://github.com/user-attachments/assets/cc12b687-b664-4497-bf91-0ab17f37bfa0)

Merged



13/05/2025::
=================

Jenkins Introductiion::
=============================

Jenkins is a free and open source automation server/tool. It helps automate the parts of software development related to building, testing, and deploying, facilitating continuous integration and continuous delivery.


Jenkins is a Orchestration tool

Jenkins is a CI/CD tool

Jenkins is a Schedular

Jenkins is a crone job schedular 


![image](https://github.com/user-attachments/assets/719a5280-bf45-435a-89b3-3675546185b1)

![image](https://github.com/user-attachments/assets/83839275-2d96-4676-b149-2b7dfe664457)


![image](https://github.com/user-attachments/assets/9ee86d60-3e25-40a2-8d45-3bfe67668a2e)


LLE/Pre-prod/UAT/PROD  ---automatically ---contunutineus deployemt


LLE/Pre-prod/UAT /PROD ---Manually ---contunutineus delivery

Roles And Responsibilities::
===============================

1)The devops engineer was responsibility to release the product to the market as soon as possible
2)release the product speed to the market
3)Devops engineer was give continues feedback to the developers
4) Devops engineer responsibility start from git and end with production

A) when your activity start from git and end with production environment(production servers)Continues deployment
when your activity start from git to LLE(lower level environment,testing environment,pre-prod…et) environment(pre-production servers)Continues delivery non-production environment


Tutorials::

https://www.tutorialspoint.com/jenkins/jenkins_overview.htm
https://www.geeksforgeeks.org/jenkins-tutorial/#prerequisites




14/05/2025::
===============


Download JDK 17 ::

https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html

Windows x64 Installer	153.92 MB	

https://download.oracle.com/java/17/archive/jdk-17.0.12_windows-x64_bin.exe (sha256 )

OR

Windows x64 Compressed Archive	172.87 MB	

https://download.oracle.com/java/17/archive/jdk-17.0.12_windows-x64_bin.zip (sha256 )

Download Maven::

https://maven.apache.org/download.cgi

Source zip archive	apache-maven-3.9.9-src.zip


====================

JDK 17 Environment setup::

Go to Search box & type Edit the system environemnt variables and click


![image](https://github.com/user-attachments/assets/66f98991-dc2a-4bd5-a093-67b88997e851)

It will navigate to System properties 

![image](https://github.com/user-attachments/assets/2b14fcee-1b5d-4f00-ac6e-b0ee83932384)

Open Environemnt Variables

![image](https://github.com/user-attachments/assets/5c2b431e-caa8-4a64-86ed-71f379f57c7b)

![image](https://github.com/user-attachments/assets/b3e2a06a-27ec-46a2-b1ac-8579c5be9321)


User variables::

JAVA_HOME=C:\Users\HP\Downloads\jdk-17.0.12_windows-x64_bin\jdk-17.0.12
 
![image](https://github.com/user-attachments/assets/8ad54751-f25d-4a0c-9339-1e90caa81094)

System variable::

%JAVA_HOME%\bin

%MAVEN_HOME%\bin
 
![image](https://github.com/user-attachments/assets/00ace73f-2dad-442d-9404-7ade62e0ba70)

![image](https://github.com/user-attachments/assets/14ea70d3-2d24-4f7d-a752-c412d4fb704d)


Maven setup::

MAVEN_HOME=C:\Users\HP\Downloads\apache-maven-3.9.9-bin\apache-maven-3.9.9

![image](https://github.com/user-attachments/assets/8a0f15af-32c5-4624-af43-59959b02e8c8)

Download link

https://maven.apache.org/download.cgi


Make sure we should setup the path at system variable 

JAVA_HOME & MAVEN_HOME

![image](https://github.com/user-attachments/assets/07ddf2ff-a7f1-470b-b07c-66316e8b1d7e)


now verify the java version & maven version:: go to git bash and verify. below are refreenced screenshots

> java -version

![image](https://github.com/user-attachments/assets/4319ddcf-5a6a-4844-aa74-5e7e3b88d601)

> mvn -v

![image](https://github.com/user-attachments/assets/ff578d8a-5c15-4686-8fdf-d9c94240ee73)


once above setup is ready then we will proceed to installe jenkins 

================

Installed jenkins in Windows::

https://www.jenkins.io/download/

Go to google search -->download jenkins war file for windows

![image](https://github.com/user-attachments/assets/d5550fe2-9af0-4376-af1b-6d4056beafe8)

Click --->WAR file link


![image](https://github.com/user-attachments/assets/3504e05f-6c0d-47a8-9b51-dffbcd0f790f)

Please follow the below link steps to installed jenkins in your windows machines

https://www.jenkins.io/doc/book/installing/war-file/

Steps::

https://www.jenkins.io/download/
1. First download the jenkins.war file and right click -->open gitbash here
  
3. run the command  -->java -jar jenkins.war --httpPort=9090

![image](https://github.com/user-attachments/assets/1cf75767-d6d7-4dfb-9a75-ccb9365b5ffb)

Browse to http://localhost:9090 and wait until the Unlock Jenkins page appears

Installed the default suggested plugins

![image](https://github.com/user-attachments/assets/081c44fc-a6a3-46fa-82e3-7b34c2dc2dd6)

click on continue 

Need to create jenkins user profile 

USER Name--->admin (any name you can provide)

PASSWORD  -->admin  (any password as your wish but make sure you should remembered the these credentials)

![image](https://github.com/user-attachments/assets/f0458a88-da81-4d32-9f87-42458fd214a1)




15/05/2025::
==============


Steps::

1.first we need to create New repository in Github

2.please Clone the Empty Repositoy in your local system

3.copy the Spring-petclinic project code to in your repository 

4.once done we need to push project code to github repository 

5. we need to integarte Github to Jenkins

we need to create Sample demo Project in Jenkins

Create sample Freestyle project::
============================

Click New Item

![image](https://github.com/user-attachments/assets/d9e7f707-aa00-4c74-b9ca-30489ded6f55)


Configuration stages::

1.General

2.Source code management (SCM)

3.Triggres

4.Environment

5.Build Steps

6.Post Build Actions


![image](https://github.com/user-attachments/assets/b7b5caf1-3d81-4de0-aebc-c2dc5080f916)


General Section provide the Project/job description 


At SCM stage level select the Git and provide the github details

![image](https://github.com/user-attachments/assets/827c5b34-8a6e-41ad-b6e1-4899348730d6)

Branches to build

![image](https://github.com/user-attachments/assets/51cf678c-afbd-40bc-bbb5-fae55e4c5537)


![image](https://github.com/user-attachments/assets/7bab6e2d-7868-460e-bd42-b2697195f3fe)

Build steps::select the Invoke top-level Maven targets
Goals section
>mvn clean install

Maven goals::

>mvn test

>mvn install


>mvn clean install


>mvn clean


>mvn package

![image](https://github.com/user-attachments/assets/53d49170-9dfe-4cad-abc0-50bf268e96c7)


Job will be created

Click Build Now


Buils is Inprogress

![image](https://github.com/user-attachments/assets/c6e399ce-ac52-47de-94a3-b4d6d156dce5)


LAB:::

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2
$ git clone git@github.com:srinfotech7358/SR-Infotech-Demo.git
Cloning into 'SR-Infotech-Demo'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2
$ cd SR-Infotech-Demo/

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (main)
$ git checkout feature/2025.05.15
branch 'feature/2025.05.15' set up to track 'origin/feature/2025.05.15'.
Switched to a new branch 'feature/2025.05.15'

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git status
On branch feature/2025.05.15
Your branch is up to date with 'origin/feature/2025.05.15'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        spring-petclinic/

nothing added to commit but untracked files present (use "git add" to track)

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git add --all
warning: adding embedded git repository: spring-petclinic
hint: You've added another git repository inside your current repository.
hint: Clones of the outer repository will not contain the contents of
hint: the embedded repository and will not know how to obtain it.
hint: If you meant to add a submodule, use:
hint:
hint:   git submodule add <url> spring-petclinic
hint:
hint: If you added this path by mistake, you can remove it from the
hint: index with:
hint:
hint:   git rm --cached spring-petclinic
hint:
hint: See "git help submodule" for more information.
hint: Disable this message with "git config set advice.addEmbeddedRepo false"

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git status
On branch feature/2025.05.15
Your branch is up to date with 'origin/feature/2025.05.15'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   spring-petclinic


HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git commit -m "i have added new spring petclinic project"
[feature/2025.05.15 30a148c] i have added new spring petclinic project
 1 file changed, 1 insertion(+)
 create mode 160000 spring-petclinic

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 299 bytes | 9.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To github.com:srinfotech7358/SR-Infotech-Demo.git
   1a61c37..30a148c  feature/2025.05.15 -> feature/2025.05.15

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git status
On branch feature/2025.05.15
Your branch is up to date with 'origin/feature/2025.05.15'.

Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        deleted:    spring-petclinic

no changes added to commit (use "git add" and/or "git commit -a")

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git add --all

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git commit -m "i have added new spring petclinic project"
[feature/2025.05.15 b7e6d86] i have added new spring petclinic project
 1 file changed, 1 deletion(-)
 delete mode 160000 spring-petclinic

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (1/1), done.
Writing objects: 100% (2/2), 255 bytes | 51.00 KiB/s, done.
Total 2 (delta 0), reused 1 (delta 0), pack-reused 0 (from 0)
To github.com:srinfotech7358/SR-Infotech-Demo.git
   30a148c..b7e6d86  feature/2025.05.15 -> feature/2025.05.15

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git add --all

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git commit -m "i have added new spring petclinic project"
[feature/2025.05.15 b53fcd4] i have added new spring petclinic project
 124 files changed, 26870 insertions(+), 1 deletion(-)
 create mode 100644 .devcontainer/Dockerfile
 create mode 100644 .devcontainer/devcontainer.json
 create mode 100644 .editorconfig
 create mode 100644 .gitattributes
 create mode 100644 .github/dco.yml
 create mode 100644 .github/workflows/deploy-and-test-cluster.yml
 create mode 100644 .github/workflows/gradle-build.yml
 create mode 100644 .github/workflows/maven-build.yml
 create mode 100644 .gitignore
 create mode 100644 .gitpod.yml
 create mode 100644 .mvn/wrapper/maven-wrapper.properties
 create mode 100644 LICENSE.txt
 create mode 100644 build.gradle
 create mode 100644 docker-compose.yml
 create mode 100644 gradle/wrapper/gradle-wrapper.jar
 create mode 100644 gradle/wrapper/gradle-wrapper.properties
 create mode 100644 gradlew
 create mode 100644 gradlew.bat
 create mode 100644 k8s/db.yml
 create mode 100644 k8s/petclinic.yml
 create mode 100644 mvnw
 create mode 100644 mvnw.cmd
 create mode 100644 pom.xml
 create mode 100644 settings.gradle
 create mode 100644 src/checkstyle/nohttp-checkstyle-suppressions.xml
 create mode 100644 src/checkstyle/nohttp-checkstyle.xml
 create mode 100644 src/main/java/org/springframework/samples/petclinic/PetClinicApplication.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/PetClinicRuntimeHints.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/model/BaseEntity.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/model/NamedEntity.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/model/Person.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/model/package-info.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/Owner.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/OwnerController.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/OwnerRepository.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/Pet.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/PetController.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/PetType.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/PetTypeFormatter.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/PetValidator.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/Visit.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/owner/VisitController.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/system/CacheConfiguration.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/system/CrashController.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/system/WebConfiguration.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/system/WelcomeController.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/vet/Specialty.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/vet/Vet.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/vet/VetController.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/vet/VetRepository.java
 create mode 100644 src/main/java/org/springframework/samples/petclinic/vet/Vets.java
 create mode 100644 src/main/resources/application-mysql.properties
 create mode 100644 src/main/resources/application-postgres.properties
 create mode 100644 src/main/resources/application.properties
 create mode 100644 src/main/resources/banner.txt
 create mode 100644 src/main/resources/db/h2/data.sql
 create mode 100644 src/main/resources/db/h2/schema.sql
 create mode 100644 src/main/resources/db/hsqldb/data.sql
 create mode 100644 src/main/resources/db/hsqldb/schema.sql
 create mode 100644 src/main/resources/db/mysql/data.sql
 create mode 100644 src/main/resources/db/mysql/petclinic_db_setup_mysql.txt
 create mode 100644 src/main/resources/db/mysql/schema.sql
 create mode 100644 src/main/resources/db/mysql/user.sql
 create mode 100644 src/main/resources/db/postgres/data.sql
 create mode 100644 src/main/resources/db/postgres/petclinic_db_setup_postgres.txt
 create mode 100644 src/main/resources/db/postgres/schema.sql
 create mode 100644 src/main/resources/messages/messages.properties
 create mode 100644 src/main/resources/messages/messages_de.properties
 create mode 100644 src/main/resources/messages/messages_en.properties
 create mode 100644 src/main/resources/messages/messages_es.properties
 create mode 100644 src/main/resources/messages/messages_fa.properties
 create mode 100644 src/main/resources/messages/messages_ko.properties
 create mode 100644 src/main/resources/messages/messages_pt.properties
 create mode 100644 src/main/resources/messages/messages_ru.properties
 create mode 100644 src/main/resources/messages/messages_tr.properties
 create mode 100644 src/main/resources/static/resources/css/petclinic.css
 create mode 100644 src/main/resources/static/resources/fonts/montserrat-webfont.eot
 create mode 100644 src/main/resources/static/resources/fonts/montserrat-webfont.svg
 create mode 100644 src/main/resources/static/resources/fonts/montserrat-webfont.ttf
 create mode 100644 src/main/resources/static/resources/fonts/montserrat-webfont.woff
 create mode 100644 src/main/resources/static/resources/fonts/varela_round-webfont.eot
 create mode 100644 src/main/resources/static/resources/fonts/varela_round-webfont.svg
 create mode 100644 src/main/resources/static/resources/fonts/varela_round-webfont.ttf
 create mode 100644 src/main/resources/static/resources/fonts/varela_round-webfont.woff
 create mode 100644 src/main/resources/static/resources/images/favicon.png
 create mode 100644 src/main/resources/static/resources/images/pets.png
 create mode 100644 src/main/resources/static/resources/images/spring-logo-dataflow-mobile.png
 create mode 100644 src/main/resources/static/resources/images/spring-logo-dataflow.png
 create mode 100644 src/main/resources/static/resources/images/spring-logo.svg
 create mode 100644 src/main/resources/templates/error.html
 create mode 100644 src/main/resources/templates/fragments/inputField.html
 create mode 100644 src/main/resources/templates/fragments/layout.html
 create mode 100644 src/main/resources/templates/fragments/selectField.html
 create mode 100644 src/main/resources/templates/owners/createOrUpdateOwnerForm.html
 create mode 100644 src/main/resources/templates/owners/findOwners.html
 create mode 100644 src/main/resources/templates/owners/ownerDetails.html
 create mode 100644 src/main/resources/templates/owners/ownersList.html
 create mode 100644 src/main/resources/templates/pets/createOrUpdatePetForm.html
 create mode 100644 src/main/resources/templates/pets/createOrUpdateVisitForm.html
 create mode 100644 src/main/resources/templates/vets/vetList.html
 create mode 100644 src/main/resources/templates/welcome.html
 create mode 100644 src/main/scss/header.scss
 create mode 100644 src/main/scss/petclinic.scss
 create mode 100644 src/main/scss/responsive.scss
 create mode 100644 src/main/scss/typography.scss
 create mode 100644 src/test/java/org/springframework/samples/petclinic/MySqlIntegrationTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/MysqlTestApplication.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/PetClinicIntegrationTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/PostgresIntegrationTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/model/ValidatorTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/owner/OwnerControllerTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/owner/PetControllerTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/owner/PetTypeFormatterTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/owner/PetValidatorTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/owner/VisitControllerTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/service/ClinicServiceTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/service/EntityUtils.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/system/CrashControllerIntegrationTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/system/CrashControllerTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/system/I18nPropertiesSyncTest.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/vet/VetControllerTests.java
 create mode 100644 src/test/java/org/springframework/samples/petclinic/vet/VetTests.java
 create mode 100644 src/test/jmeter/petclinic_test_plan.jmx

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$ git push
Enumerating objects: 178, done.
Counting objects: 100% (178/178), done.
Delta compression using up to 4 threads
Compressing objects: 100% (160/160), done.
Writing objects: 100% (176/176), 455.71 KiB | 1.29 MiB/s, done.
Total 176 (delta 30), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (30/30), done.
To github.com:srinfotech7358/SR-Infotech-Demo.git
   b7e6d86..b53fcd4  feature/2025.05.15 -> feature/2025.05.15

HP@DESKTOP-E518Q66 MINGW64 ~/OneDrive/Documents/SR inoftech Batch2/SR-Infotech-Demo (feature/2025.05.15)
$
