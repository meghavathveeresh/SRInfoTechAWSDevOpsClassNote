

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



16/05/2025::
==================



![image](https://github.com/user-attachments/assets/61ab9296-334d-43f7-ae26-7ec251c37ba1)



Poll SCM ::Jenkins server ask git if there is any changes in git server or not, if changes there Jenkins server build/package the changes , every change build happened like 5 mints ,means every 5 minutes verify the Jenkins server to git if there is any changes 


![image](https://github.com/user-attachments/assets/2fde4c24-c07d-4b57-bdec-b75a402f1155)


![image](https://github.com/user-attachments/assets/6f436ad6-e92a-40e3-831a-23219c288217)

POLL SCM ----* * * * * --every minute when every commit 

Create one sample POLL SCM jenkins job::
===========================================
Go to jenkins Dashboard
click New Item

![image](https://github.com/user-attachments/assets/1c62657f-935b-4eed-b032-08842fb09a57)

Description

![image](https://github.com/user-attachments/assets/3a54ba69-b2aa-4443-ad9b-d18ab5fbde02)


Provide the Git URL

![image](https://github.com/user-attachments/assets/1fb7b83f-3bba-411b-aad9-a725f25d3e1c)


Branch buiild

![image](https://github.com/user-attachments/assets/71aec8f1-4783-4e97-97cb-232dd18811ae)

POLL SCM:: * * * * *

every minute build was trigger when new commits happend in github repository

![image](https://github.com/user-attachments/assets/d6ab7a34-156a-4430-9d40-31e362ad23b1)


Build Steps::

![image](https://github.com/user-attachments/assets/4aae78af-d217-41de-a1e6-16bfe2e34472)




19/05/2025::
=================


Execute the Jobs in Parallel::
==============================


1.By Default execute the Jenkins build jobs are sequence way,one by one 

2.Don’t do 2 projects build parallel  this is real time scenario but we can do parallel builds as well one job

Jenkins build parallel setup

Go job ---> configure ----> Generall ---> Execute concurrent builds if necessary

Execute concurrent builds if necessary::
===================================

When this option is checked, multiple builds of this project may be executed in parallel.
By default, only a single build of a project is executed at a time — any other requests to start building that project will remain in the build queue until the first build is complete.


![image](https://github.com/user-attachments/assets/909edd87-548d-4ded-a862-29cf850fac05)


Here 5 builds execute parallel ,I kept executor is 5 this is same machine 

![image](https://github.com/user-attachments/assets/a840a224-5cbb-43cc-92c1-d135db4ce00f)


Build Periodically:::	H/15 * * * *   ----this build happened every 5 minutes without commits ,if changes are commit or not but every 5 mints 

build happened in Jenkins 

Discard old builds::
=============

Jenkins offers two options for determining when builds should be discarded:

Build age: discard builds when they reach a certain age; for example, seven days old.
Build count: discard the oldest build when a certain number of builds already exist.
These two options can be active at the same time, so you can keep builds for 14 days, but only up to a limit of 50 builds, for example. If either limit is exceeded, then any builds beyond that limit will be discarded.

![image](https://github.com/user-attachments/assets/18264333-9ea0-41b9-9531-c90a38178e6a)



Create Sample Build peridiocally jenkins job::
=============================================

Description

![image](https://github.com/user-attachments/assets/5ad69478-039e-4ef7-a35f-cb18ed8364f1)

Git url::

![image](https://github.com/user-attachments/assets/b2cbdb7c-14ac-4fae-a240-90cc7a82c78d)

Build the branch

![image](https://github.com/user-attachments/assets/94230c57-b88f-4ab1-b894-151f30fa6d53)

every 5 mints build will trigger

Build Periodically:::	H/15 * * * *   ----this build happened every 5 minutes without commits ,if changes are commit or not but every 5 mints 

build happened in Jenkins 

![image](https://github.com/user-attachments/assets/a5321109-944b-4e79-9294-e28c2adfea0d)

click save 


Whenever you configure a build activities :::
=======================================

SCM::

	Where is your project

Build environment::

---all about your workspace folders 

Build Triggers::

--whenever code changes 
--periodic
---script calls 

Build steps::

Dev team will tell ,

Post build::

That aim is giving continue feedback to dev team

--send mails
--build pass/fail
--CI

Manage Jenkins::
=================

1.configure system

--number of executors
--E-mail notifications
--internall org SMTP

We don’t change anything in system level configurations



20/05/2025::
==============


Post build Action i want to published artifacts & test results

![image](https://github.com/user-attachments/assets/fcd3ea28-a352-431f-8e1b-86758787fe7a)

I'm going to created one free style job and configured Post-build Actions

In post build Action select the option Archive the artifacts

>target/*.war

![image](https://github.com/user-attachments/assets/39dcf26d-74ee-4c7f-bc28-bb7f6116fedb)

In post build Action select the option Publish JUnit test result report for to published the test results

>target/surefire-reports/*.xml


![image](https://github.com/user-attachments/assets/e04f371d-b684-406b-9210-50fb74b6ea79)

![image](https://github.com/user-attachments/assets/985bffcc-5212-4670-a782-0aee21a1c1a1)


I want to show test results ::
=================================


>ls target 

Post build action stage

Select archive the artifact
--target/*.jar

Junit test results::
--target/surefire-reports/*.xml


See test results & antifactory ::
===================================

![image](https://github.com/user-attachments/assets/2711b453-072e-40d2-9596-afce8f586310)


3.For every company will do sequence build on one project this is recommended approach

crone job formate link

https://crontab.guru/examples.html

Parameterized Jenkins Jobs ::
=============================

Run the same job with different inputs without modifying the configuration manually, we can go for Parameterized projects

Go To New Item

![image](https://github.com/user-attachments/assets/20b1237b-1681-4e77-ad8b-33ee8ac69b97)

Enter Job Name, Free style project and click ok

![image](https://github.com/user-attachments/assets/106bb57e-5466-4e1d-9ead-c977aaac60e7)


Enter the description

![image](https://github.com/user-attachments/assets/4944c35f-86db-42a4-8bb8-4b3d9987fd81)

Select the option This project is parameterised

![image](https://github.com/user-attachments/assets/4eeab439-3e45-4320-a7de-73360c28c3c3)

Click Add Parameter

![image](https://github.com/user-attachments/assets/3570dcc9-72a0-4034-8da3-1a70e0341fa7)

Select optiions String parameter or choise parameter or boolean parameter you can select the ny options based on your requirement 

![image](https://github.com/user-attachments/assets/210ae086-fecf-42b2-9322-966b85431d18)

select string parameter

![image](https://github.com/user-attachments/assets/aa0b6706-bda8-4de8-a094-d14e4955fc34)

Select Choise Parameter

![image](https://github.com/user-attachments/assets/48baed03-fe9c-482b-870b-ba4126eb2b4a)

choise parameter

![image](https://github.com/user-attachments/assets/a50a06a9-5063-4f12-8d10-0f44ee473f46)

Click Save

You Can observed this project is parameterized 

![image](https://github.com/user-attachments/assets/05be584b-bd82-4f00-89c7-6358a4ca5ca4)

Click Build with parameter

![image](https://github.com/user-attachments/assets/a7317486-0b18-4e78-9a64-4113f712a757)

select deployment environment

![image](https://github.com/user-attachments/assets/b12a618f-a8da-4c8f-b19c-7b92af2431da)

select which versioj you want to deployment like tis you can configured real time parameterized project in jenkins

![image](https://github.com/user-attachments/assets/33a52ced-4fa7-4b69-a0f9-a82fe436cdfd)

Click Build

![image](https://github.com/user-attachments/assets/7acf8c06-b734-4512-acf7-86ed9fd9053a)

![image](https://github.com/user-attachments/assets/1cec807a-76cc-4446-a589-4767563b90eb)




21/05/2025::
===============


I want Build a 3 projects ::
===========================



![image](https://github.com/user-attachments/assets/b2dfde9d-e397-46b8-a8cb-67ab3711b141)


Project-A, Projec -B, Projec - C 

Once Project-A build is done, then it will start Project-B build and once Project-B build SUccess then it will start Project-C build ---for this we need to select Add post-build action and select "Build other projects" in drop down and provide Project-B details.


![image](https://github.com/user-attachments/assets/048a99bc-bcf6-47ca-9b27-ef23152eab97)


Projec A is  (Downstream project is ---Projec B)

Projec B is (UP Stream project is ----Projec A)

Projec C is (downstream project of --Projec B)

i created 3 free style project in jenkins 

Project-A ::
==============

Github URL::: https://github.com/parasa7358/spring-petclinic.git

![image](https://github.com/user-attachments/assets/e8073061-b815-4945-bd7f-c20b3a6576e2)

Post Build Action , select the option Build Other Project  Project-B

![image](https://github.com/user-attachments/assets/ef75f777-c273-4255-b063-f9853072dfcb)

Project -B ::
=============

Github URL:::https://github.com/parasa7358/onlinebookstore.git

![image](https://github.com/user-attachments/assets/2ee62e92-e677-4717-93be-77d6dd1ecbf9)

Post Build Action , select the option Build Other Project Project-C

![image](https://github.com/user-attachments/assets/ec7cfc18-002b-4dc3-8438-a75b12b9a438)


Project-C::
============


Github URL:::https://github.com/srinfotech7358/shopping-cart


22/05/2025::
================


Pipelines Introduction:::

A Jenkins pipeline is a series of automated steps or stages that define the process of continuous integration/continuous delivery (CI/CD) for your code. Jenkins, being a popular open-source automation server, uses pipelines to automate tasks like building, testing, and deploying code.

There are two types of Jenkins pipelines:

1. Declarative Pipeline
2. Scripted Pipeline

1. Declarative Pipeline::
The declarative pipeline syntax is simpler and more structured. It's the recommended style for most users because it's easy to read and maintain

Create Pipeline Project::
=======================

Steps

Click +New Item


![image](https://github.com/user-attachments/assets/43694be8-ac77-41a1-9d90-30175a91443f)

Enter the Project Name And Click OK

![image](https://github.com/user-attachments/assets/b21659a3-ff70-46ff-86b0-7a965b48197a)

At General Section Provide the Description

![image](https://github.com/user-attachments/assets/e0c5db89-597c-439e-91e1-7722bd4d5467)


At Definition, We need to select the Pipeline Script 

![image](https://github.com/user-attachments/assets/f9b35819-0b40-4d71-9678-949d35a4cd3e)



Here's an example of a simple declarative pipeline: Syntax

pipeline{

agent any

stages{

Stage ('Clone'){

steps{

// write code
}
}

Stage ('Build'){
steps{

// write code
}
// write code

}

Stage ('Test'){

steps{

// write code
}
// write code

}
Stage ('Execute test casea and get the results'){

steps{

// write code
}
// write code

}

Stage ('Generated Artifact'){

steps{

// write code
}
// write code

}

Stage ('Deploy'){

steps{

// write code
}
// write code

}

// write code

}

}

Please try to create one pipeline job in jenkinsfile and execute the below Declarative pipeline example:;


pipeline {

   agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/srinfotech7358/spring-petclinic.git'
            }
        }
        
          stage('Build') {
            steps {
               bat 'mvn clean install'
            }
        }
          stage('Test') {
            steps {
               bat 'mvn test'
            }
        }
        
          stage('Generate Junit Test Results') {
            steps {
               junit 'target/surefire-reports/*.xml'
            }
        }
        
          stage('Generate Artifacts') {
            steps {
               archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
            }
        }
    }
}


Plugins::
===============

Plugins in Jenkins are essential components that extend its core functionality, allowing you to customize Jenkins to meet specific CI/CD needs. Jenkins has a vast plugin ecosystem that supports building, deploying, and automating software projects across various platforms and tools

Install Plugins in Jenkins::
==============================

Step-by-Step:
Log in to Jenkins as an administrator.

Navigate to Manage Jenkins (usually on the left sidebar).

Click on Manage Plugins.

(Image reference from Jenkins documentation)

Go to the Available tab.

Use the search box to find the plugin you want.

Check the box next to the plugin name.

Click:

Pipeline: Stage View::
=================

Pipeline: Stage View Plugin in Jenkins
The Pipeline: Stage View plugin is a visualization tool in Jenkins that allows users to see a graphical view of each stage in a pipeline. It provides a real-time and historical overview of pipeline execution per stage, making it easier to debug, monitor, and analyze performance.


Click the Build Now and we can triggered the pipeline

![image](https://github.com/user-attachments/assets/4e211efb-fafe-4598-b29c-bb4bd5d488f2)

![image](https://github.com/user-attachments/assets/04315f1c-44ff-4078-952b-38320fec68c8)

Success all the stages & Steps

![image](https://github.com/user-attachments/assets/318c9d53-56fc-4815-9205-74d4dac0bf28)


Key elements in the declarative pipeline:::
======================================
pipeline: This is the top-level structure.

agent: Specifies where the pipeline will run, such as on any available agent, a specific node, or a Docker container.

stages: Defines the different steps or stages in the pipeline (e.g., Build, Test, Deploy).

steps: Commands to be executed in each stage.



23/05/2025::
==============


2. Scripted Pipeline::
   ==============

The scripted pipeline offers more flexibility, but it is less structured and can be harder to maintain. It uses Groovy syntax to define the pipeline.

Here's an example of a scripted pipeline:

node {
    try {
        stage('Build') {
            echo 'Building the application...'
            // Your build commands here
        }
        
        stage('Test') {
            echo 'Running tests...'
            // Your test commands here
        }

        stage('Deploy') {
            echo 'Deploying the application...'
            // Your deploy commands here
        }


        Please try to create one new jenkins pipeline job and execute below script for Scripted pipeline examples

        node {
        stage('Clone') {
                git branch: 'master', url: 'https://github.com/parasa7358/onlinebookstore.git'
			}
			
			 stage('Build') {
        
                bat 'mvn package'
        
			}
			stage('Test') {
        
                bat 'mvn test'
        
			}
        }



  Key differences in a scripted pipeline:::
  ==================================
node: Represents a Jenkins agent where the pipeline will run.

Pipeline as Code::
==================
Both declarative and scripted pipelines are stored as Jenkinsfiles, which you place in your source code repository. This allows you to version control your pipeline and keep it aligned with your application code.

Declarative pipeline with Jenkinsfile::
===============================

pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'git@github.com:parasa7358/spring-petclinic.git'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn package'
            }
        }
        
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Test Results Reports') {
            steps {
                junit 'target/surefire-reports/*.xml'
            }
        }
        
        stage('Artifacts') {
            steps {
                archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
            }
        }
        stage('Deploy') {
            steps {
                echo 'Hello World'
            }
        }
    }
}


This pipeline:::

1 Checks out the source code from your Git repository.
2. Builds the project using Maven.
3.Runs unit tests.
4.Deploys the application using a custom script.

JOb creation::

![image](https://github.com/user-attachments/assets/dacaf03a-5557-44ce-88ba-0b230ed061cb)

Branches to build

![image](https://github.com/user-attachments/assets/64065ba7-534e-4771-a667-00d5f64e5a4b)

Script Path::: This path is Jenkinsfiles where we maintained in github source code level

![image](https://github.com/user-attachments/assets/3b4783f0-c613-45d1-81a7-00712a79f5ad)


Scripted pipeline with Jenkinsfile::
===============================

node {
    
        stage('Clone') {
           
                git branch: 'main', url: 'git@github.com:parasa7358/spring-petclinic.git' 
        }
        stage('Build') {
          
                bat 'mvn package'
        }
        
        stage('Test') {
          
                bat 'mvn test'
        }
        stage('Test Results Reports') {
           
                junit 'target/surefire-reports/*.xml'
        }
        
        stage('Artifacts') {
          
                archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
        }
        stage('Deploy') {
          
                echo 'Hello World'
        }
    }


github sourcecode jenkinsfile 

![image](https://github.com/user-attachments/assets/44f93ca7-1d95-4efb-afad-cc262de61dbe)



26/05/2025::
=================


Tomcat Web Server: Introduction
===============

Apache Tomcat is an open-source web server and servlet container developed by the Apache Software Foundation. It is primarily used to serve Java applications and is one of the most popular servlet containers in the world.

Tomcat is an essential tool for anyone working with Java web applications. It provides a simple, reliable platform for deploying and managing Java Servlets and JSPs and is widely used in both development and production environments. Its ease of use, combined with powerful features and flexibility, makes it an ideal choice for many developers working on Java-based web applications.

Apache Tomcat is an open-source web server and servlet container that is primarily used to serve Java-based web applications. It implements several Java EE (Enterprise Edition) specifications, such as Java Servlet, JavaServer Pages (JSP), and WebSocket, among others. Tomcat is often used to run Java applications on the web because it's lightweight, easy to configure, and widely supported.

Here are some key points about Tomcat:

1. **Servlet Container**: Tomcat is a servlet container, meaning it manages the lifecycle of Java Servlets, which are small Java programs that run on a web server.
  
2. **JSP Support**: Tomcat also supports JavaServer Pages (JSP), a technology that allows for embedding Java code within HTML pages.

3. **Configuration**: It’s highly configurable through XML files, like `server.xml` for server settings, `web.xml` for application settings, and others.

4. **Lightweight**: Unlike full-fledged application servers like WildFly (formerly JBoss) or GlassFish, Tomcat is primarily a servlet and JSP container, which makes it lighter and easier to deploy for simpler Java web applications.

5. **Performance**: It’s known for good performance in handling static content, making it a popular choice for Java web developers.


Tomcat Download link::
--------------------

https://tomcat.apache.org/download-90.cgi


64-bit Windows zip

![image](https://github.com/user-attachments/assets/bba6eafd-95c3-4963-a862-b4b97bb8cd24)

after downloaded the tomcat ,we need extrack the all the files

![image](https://github.com/user-attachments/assets/b2b88b1d-ef2b-4a98-9784-a5e4c3d7a8ad)

![image](https://github.com/user-attachments/assets/f3bde035-5e36-4ab8-af12-8a0b3f6a20c1)

go to bin folder

C:\Users\HP\Downloads\apache-tomcat-9.0.105-windows-x64\apache-tomcat-9.0.105\bin

![image](https://github.com/user-attachments/assets/6e6ffef2-c57a-40f5-8f08-4e16e8211cad)

navigate to CMD--command prompt


![image](https://github.com/user-attachments/assets/3f4ee311-5580-40ce-976c-ff4263ab3304)


run the command

>startup.bat

![image](https://github.com/user-attachments/assets/fd4ffdc2-793f-448a-8b38-9997f67aea7c)


we can find tomcat server started

![image](https://github.com/user-attachments/assets/1c229015-e118-4f25-ae64-c36d640aeed5)

we can navigate to browser

http://localhost:8080/

![image](https://github.com/user-attachments/assets/21b3cc58-d242-4955-8e9f-5e27c626bc2d)


![image](https://github.com/user-attachments/assets/27e7023b-7544-41eb-9ed3-f04d2680d318)


Integrate Tomcat Jenkins::
==============================



![image](https://github.com/user-attachments/assets/7155f817-58cd-4f85-93e8-405b7c96fd7b)


Integrating Tomcat with Jenkins is a common use case for automating the deployment of Java-based web applications. Jenkins can be set up to deploy a web application to a Tomcat server whenever a new build is triggered.

Prerequisites:

Apache Tomcat should be installed and running on your server.
Jenkins should be installed and running.

Steps to integrate Jenkins with Tomcat:

1. Install the "Deploy to Container" Plugin in Jenkins:
The easiest way to deploy to Tomcat from Jenkins is by using the Deploy to Container plugin. This plugin allows Jenkins to deploy WAR files to a Tomcat server.

Go to your Jenkins dashboard.
Click on Manage Jenkins > Manage Plugins.
In the Available tab, search for Deploy to Container Plugin and install it.
Once installed, restart Jenkins to apply the plugin.

2. Configure Tomcat Server in Jenkins:
Now you need to tell Jenkins where your Tomcat server is running.

In Jenkins, go to Manage Jenkins > Configure System.
Scroll down to the Deploy to container section.
Click Add Tomcat Server.

Provide the necessary information:
Name: Give the Tomcat server a name (Tomcat9).
URL: The URL of your Tomcat server (e.g., http://localhost:8080).
Username: The username for Tomcat's manager app (usually admin).
Password: The password for that username (set in Tomcat's tomcat-users.xml).
Save the configuration.

3. Configure Tomcat’s tomcat-users.xml:
Make sure Tomcat is set up to allow Jenkins to deploy the application by editing the tomcat-users.xml file.

https://stackoverflow.com/questions/7763560/401-unauthorized-error-while-logging-in-manager-app-of-tomcat

tomcat-users.xml file::
=========================

![image](https://github.com/user-attachments/assets/61a0b6ae-1e6c-47d0-8852-b226d65f38a4)



  <role rolename="manager-gui"/>
  <role rolename="manager-script"/>
  <role rolename="manager-jmx"/>
  <role rolename="manager-status"/>
  <role rolename="admin-gui"/>
  <role rolename="admin-script"/>
  <user username="admin" password="admin" roles="manager-gui, manager-script, manager-jmx, manager-status, admin-gui, admin-script"/>




Restart Tomcat to apply the changes.

4. Create a Jenkins Job to Build and Deploy the Application:
Next, you need to create a Jenkins job that will build your web application (e.g., a WAR file) and deploy it to Tomcat.

From the Jenkins dashboard, click New Item.

Select Freestyle Project, give it a name, and click OK.

>TomcatServer Integrate With Jenkins

In the job configuration, go to the Build section and configure your build step, such as building a Maven project For Maven, you can use:

> mvn clean install

In the Post-build Actions section, add Deploy war/ear to a container.

In the WAR/EAR files field, provide the path to your WAR file (e.g., target/*.war).
In the Container field, choose the Tomcat server you configured earlier.
Set the Context Path (e.g., TomcatIntegartedWithJenkins), which is the URL path where the application will be accessible on Tomcat.
If you want Jenkins to deploy automatically after every successful build, check the option Deploy after every successful build.

please use below project to configured Tomcat integration

https://github.com/ifocusbatch2/Petclinic.git

![image](https://github.com/user-attachments/assets/0692c308-09f1-4dec-9db7-b5c280e1b93c)


build steps

![image](https://github.com/user-attachments/assets/bf5bc2fc-7b95-48d4-9a35-cf074d6a2b33)

Post-build Actions

please select Deploy war/ear to a container in drop down


![image](https://github.com/user-attachments/assets/76756b66-a6a1-4178-911c-47c17e345695)

WAR/EAR files::: target/*.war

Context path:::TomcatIntegartedWithJenkins

containers::Tomcat 9.x Remote

please add tomcat credentials username and password

![image](https://github.com/user-attachments/assets/5641604b-6c0f-43c1-8249-0f96c0db8560)

Tomcat URL ::http://localhost:8080/

![image](https://github.com/user-attachments/assets/f3b90910-86d6-4c79-a015-843c05ba68d4)


![image](https://github.com/user-attachments/assets/68a490c3-37e1-427f-bade-e84ad096c991)


Save the job.

5. Trigger the Build and Deployment:
Go to the Jenkins job you just created and click Build Now to trigger a build.
After the build completes, Jenkins should deploy the WAR file to your Tomcat server.

![image](https://github.com/user-attachments/assets/e6ba9811-d613-47e7-bb7b-497ca0d2799c)


build success

[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  06:16 min
[INFO] Finished at: 2025-05-26T11:12:07+05:30
[INFO] ------------------------------------------------------------------------
[DeployPublisher][INFO] Attempting to deploy 1 war file(s)
[DeployPublisher][INFO] Deploying C:\Users\HP\.jenkins\workspace\TomcatServer Integrate With Jenkins\target\petclinic.war to container Tomcat 9.x Remote with context TomcatIntegartedWithJenkins
  Redeploying [C:\Users\HP\.jenkins\workspace\TomcatServer Integrate With Jenkins\target\petclinic.war]
  Undeploying [C:\Users\HP\.jenkins\workspace\TomcatServer Integrate With Jenkins\target\petclinic.war]
  Deploying [C:\Users\HP\.jenkins\workspace\TomcatServer Integrate With Jenkins\target\petclinic.war]
Finished: SUCCESS

![image](https://github.com/user-attachments/assets/61019ca1-6464-413d-9e26-34a0af06646c)

Once Build & Deployemnt completed go to Tomcat Server

http://localhost:8080/

Click Manager App

![image](https://github.com/user-attachments/assets/58cacf90-e7c7-4200-9f05-25826ca96555)

You should found /TomcatIntegartedWithJenkins

![image](https://github.com/user-attachments/assets/c600da43-55b3-4518-a350-bf1a2e7e4fc8)

click /TomcatIntegartedWithJenkins


Spring-petclinic web application up & running

![image](https://github.com/user-attachments/assets/7a4eaebc-e149-4817-9bf9-70ad3a4e93c5)



27/05/2025::
=================


Polling SCM (Source Code Management) and webhooks are two common methods used for integrating continuous integration (CI) systems or automating tasks based on changes in repositories.

1. Polling SCM
Polling SCM is a method where a system (like Jenkins, GitLab CI, etc.) periodically checks the source code repository for changes. If it detects changes, it triggers the build process or some other automated task.

How it works:

A job is set up to check the SCM (like GitHub, GitLab, Bitbucket, etc.) at regular intervals (e.g., every minute or hour).

The CI server pulls the repository to see if there are any new commits since the last poll.

If changes are detected, it triggers the CI/CD pipeline to build, test, or deploy the application.

2. Webhooks
Webhooks provide a more efficient method for triggering actions based on changes in the repository. Rather than the CI system polling for changes, the source control platform sends an HTTP POST request (webhook) to the CI system when an event (like a commit or pull request) occurs.

![image](https://github.com/user-attachments/assets/59e3f392-4da9-4fe3-8238-d2bd2fee5fc3)


Deploy Onlinebookstore/spring-petclinic applications to target server (Tomcat)::
=====================================================================================================================

please create one new pipeline job

Provide the Description

![image](https://github.com/user-attachments/assets/458b8076-ebce-4ac0-932e-64ee5a6e460b)

Enabled POLL SCM

![image](https://github.com/user-attachments/assets/5b5ae6d9-987a-4c54-9450-c3a89497be29)

In Pipeline Section write groovy script using Declarative style 


![image](https://github.com/user-attachments/assets/5d624b7b-9224-4d20-863f-0f3e4671916e)


Generate Deploy pipeline script::
====================================




Script::
=======

pipeline
{
    agent any

    tools{

        maven 'maven'
    }

stages{
stage('Git checkout'){

    steps{

        git branch: 'main' url: 'https://github.com/parasa7358/Petclinic.git'

    }
}

stage('clean and install'){

    steps{

      sh 'mvn clean install'

    }
}

stage('Package'){

    steps{

      sh 'mvn package'

    }
}

stage('Archive the Artifacts'){

    steps{

      sh 'mvn clean install'
    }
    post{
        success{

            archiveArtifacts artifacts: '**target/*.war'
        }
    }

    }


stage('Test Cases'){

    steps{

      sh 'mvn test'

    }
}


stage('Deploy to tomcat server'){

    steps{

      deploy adapters: [tomcat9(credentialsId: 'tomcat9credentials', path: '', url: 'http://localhost:8080/')], contextPath: 'SRINFOTECH', war: '**/*.war'

    }
}

}
}


Run the job


![image](https://github.com/user-attachments/assets/f240a720-41dd-4bc0-955d-a247b1cf8918)

![image](https://github.com/user-attachments/assets/369955cf-0f1c-4ae1-bae3-3870edc0e282)

Integrate Jenkins with Tomcat using Declarative Approach::
============================================

To integrate Jenkins with Tomcat using the Declarative Pipeline approach, you'll be using Jenkins Pipeline syntax to automate the deployment process to a Tomcat server. This process typically involves building the application, packaging it, and then deploying it to Tomcat.

1. Jenkinsfile Configuration (Declarative Pipeline)

In your Jenkins project, you'll create a Jenkinsfile, which contains the Declarative Pipeline syntax. This file defines the steps involved in the CI/CD pipeline.

Please execute below script in jenkins pipeline job using Declarative style

pipeline
{
    agent any

    tools{

        maven 'maven'
    }

stages{
stage('Git checkout'){

    steps{

        git branch: 'feature/2025.03.12', url: 'https://github.com/parasa7358/Petclinic.git'

    }
}

stage('clean and install'){

    steps{

      sh 'mvn clean install'

    }
}

stage('Package'){

    steps{

      sh 'mvn package'

    }
}

stage('Archive the Artifacts'){

    steps{

      sh 'mvn clean install'
    }
    post{
        success{

            archiveArtifacts artifacts: '**target/*.war'
        }
    }

    }


stage('Test Cases'){

    steps{

      sh 'mvn test'

    }
}


stage('Deploy to tomcat server'){

    steps{

      deploy adapters: [tomcat9(credentialsId: 'tomcat9credentials', path: '', url: 'http://localhost:8080/')], contextPath: 'SRINFOTECH', war: '**/*.war'

    }
}

}
}


Onlinebookstore::

 pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'master', url: 'https://github.com/srinfotech7358/onlinebookstore.git'
            }
        }
        
          stage('Build') {
            steps {
               bat 'mvn clean install'
            }
        }
         stage('Generate Artifacts') {
            steps {
               archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
            }
        }

          stage('Deploy to Tomcat Server') {
            steps {
               deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'Tomcat', path: '', url: 'http://localhost:8080')], contextPath: 'SR INFOTECH SOLUTIONS PVT LIMITED', war: 'target/*.war'
            }
        }
    }
}



28/08/2025::
==============

SonarQube::
===============

Sonarqube installed link::

https://gist.github.com/dmancloud/0abf6ad0cb16e1bce2e907f457c8fce9

default U/P ---admin/admin


![image](https://github.com/user-attachments/assets/f248e676-0498-4286-b7b0-43f78bddabd2)


To integrate SonarQube with Jenkins, you need to ensure that Jenkins can communicate with your SonarQube server to perform static code analysis during your CI/CD pipeline. This will allow you to analyze your code quality and get reports from SonarQube as part of your build process.

Here's how you can integrate SonarQube with Jenkins:please follow below steps

1. Install the SonarQube Plugin in Jenkins
Before you start, ensure that you have the SonarQube Scanner Plugin installed in Jenkins:

Go to Jenkins Dashboard.
Click on Manage Jenkins → Plugins.
Go to the Available tab, and search for SonarQube Scanner.
Install it and restart Jenkins.

2. Configure SonarQube in Jenkins
Next, you need to configure SonarQube on Jenkins so it can communicate with your SonarQube server.

Steps:
=====
Go to Jenkins Dashboard.
Click on Manage Jenkins → Configure System.
Scroll down to the SonarQube servers section and click Add SonarQube.

Fill in the following details:
=======================
Name::: Give your SonarQube instance a name (SonarQubeServer).
Server URL: URL to your SonarQube instance (e.g., http://localhost:9000). and default port is 9000
Server Authentication Token: You can generate a token in SonarQube by navigating to My Account → Security → Generate Tokens. Paste this token into Jenkins.
Click Save.

3. Configure the SonarQube Scanner in JenkinsSteps:
 ===============================================
In the Configure System page, scroll to the SonarQube Scanner section.
Click Add SonarQube Scanner and select SonarQube Scanner for Jenkins.

If you want to use a custom installation, specify the path to the SonarQube Scanner binary.
Click Save.

 Configure SonarQube Project::
 ========================
Go to your SonarQube server (e.g., http://localhost:9000).
Create a project or use an existing one.
Obtain the Project Key from the SonarQube project and update the pipeline script as shown in the sonar.projectKey parameter.

Go to Projects and click Local project

![image](https://github.com/user-attachments/assets/0b177021-0fc2-4ba4-a987-fee4a3420717)

Click Next

![image](https://github.com/user-attachments/assets/2cccbec2-463b-47ab-9379-f02244272f3a)

Selected Use the global setting

![image](https://github.com/user-attachments/assets/702766f0-01a9-4919-bbda-acb3a8996dcd)

Click Create Project

![image](https://github.com/user-attachments/assets/a614a64f-7171-43c3-b19e-787e13ee0c16)

Now Spring-petclinic Project created in Sonarqube

![image](https://github.com/user-attachments/assets/0f79347c-8bde-4fa3-8eaa-3ca91a27422d)

Click Locally

![image](https://github.com/user-attachments/assets/d6e4fa35-299c-4768-b291-c669d9b52995)

![image](https://github.com/user-attachments/assets/ba49dbeb-8f7f-4fb4-ab7d-8c4d3644a133)

Click Generate for Token

Analyze "spring-petclinic12": sqp_0eb364758c5186bea4077eff841ddb99ba89a3ab


![image](https://github.com/user-attachments/assets/7e46dded-06da-467a-8838-62e9f0337a7a)

Click Continue

![image](https://github.com/user-attachments/assets/590c723c-0df3-48df-bf7d-77575e63614a)

![image](https://github.com/user-attachments/assets/ace61156-d25b-4d00-b248-d5bd0b1de835)

Selected Maven and copy below script from sonarqube and it will help to integrate Sonarqube with jenkins pipeline

![image](https://github.com/user-attachments/assets/1da2fbb2-5118-45e5-85ec-c7767a44529b)


mvn clean verify sonar:sonar \
  -Dsonar.projectKey=spring-petclinic12 \
  -Dsonar.projectName='spring-petclinic12' \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.token=sqp_0eb364758c5186bea4077eff841ddb99ba89a3ab


29/05/2025::
===============

 IntegrateSonarqubeWithJenkins::
  ==================================

  Go To jenkins and create new job IntegrateSonarqubeWithJenkins

  ![image](https://github.com/user-attachments/assets/dc7d3f1e-5852-4288-bf00-5537b6a4935c)

Please use below script to run the pipeline job

pipeline
{
    agent any

    tools{

        maven 'maven'
    }

stages{
stage('Git checkout'){

    steps{

        git branch: 'main', url: 'https://github.com/parasa7358/Petclinic.git'

    }
}

stage('clean and install'){

    steps{

      bat 'mvn clean install'

    }
}

stage('Package'){

    steps{

      bat 'mvn package'

    }
}

stage('Archive the Artifacts'){

    steps{

      bat 'mvn clean install'
    }
    post{
        success{

            archiveArtifacts artifacts: '**target/*.war'
        }
    }

    }


stage('Test Cases'){

    steps{

      bat 'mvn test'

    }
}

stage('Sonarqube Analysis'){

    steps{

      bat 'mvn clean package'

    bat '''mvn sonar:sonar \
  -Dsonar.projectKey=spring-petclinic \
  -Dsonar.projectName='spring-petclinic' \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.token=sqp_8d74d659dbf3d3bf2924a0d24104f5ddba914fac'''

    }
}


stage('Deploy to tomcat server'){

    steps{

      deploy adapters: [tomcat9(credentialsId: 'tomcat9credentials', path: '', url: 'http://localhost:8080/')], contextPath: 'Ifocus Solutions Pvt Ltd', war: '**/*.war'

    }
}

}
}



  02/06/2025::
  ==================

1. please start Jenkins on your machine & make sure Jenkins server is UP & Running state
2. please start Tomcat on your machine & make sure Tomcat server is UP & Running state
3. please start Sonarqube on your machine & make sure Sonarqube server is UP & Running state

once above steps done then we can execute below script

Working Scripts CI/CD::
===========================

pipeline{

    tools{

        maven 'Maven'
    }
agent any

stages{

    stage('Clone'){

        steps{

            git branch: 'main', url: 'https://github.com/srinfotech7358/Petclinic.git'
        }
    }

     stage('Build') {
            steps {
               bat 'mvn clean install'
            }
        }

         stage('Test Cases') {
            steps {
               bat 'mvn test'
            }
        }

         stage('Archive the Artifacts') {
            steps {
               archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
            }
        }
 stage('Sonarqube Analysis') {
            steps {
               
               bat 'mvn package'
              bat '''mvn sonar:sonar \
             -Dsonar.projectKey=spring-petclinic \
             -Dsonar.projectName='spring-petclinic' \
            -Dsonar.host.url=http://localhost:9000 \
            -Dsonar.token=sqp_96cf5222ab632b69c14baa5590210a7125185d5a'''
            }
        }


 stage('Deploy Application into Tomcat Server') {
            steps {
               deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'NewTomcat', path: '', url: 'http://localhost:8080/')], contextPath: 'Test', war: 'target/*.war'
            }
        }

}

}


Once sonarqube scanner done, please verify the sonarqube dashboard for reports & results

![image](https://github.com/user-attachments/assets/acc53857-78ca-4e07-becc-6aba969c61b4)

Go to Administration

![image](https://github.com/user-attachments/assets/e94cc57e-d8fe-4d4a-8110-6a0afa2164af)


Click Projects & Select Background Tasks


![image](https://github.com/user-attachments/assets/53d35e0d-abe2-462e-a608-4736b3cd06c4)

You can able to see all scanned projects status

![image](https://github.com/user-attachments/assets/7075a240-88a1-4c2b-b68d-c963e8f666aa)

Click on any Project, see the PASSED the quality gates

![image](https://github.com/user-attachments/assets/0d329366-3a10-4131-b5a4-e2fb7063647d)

Click on Overall Code option

![image](https://github.com/user-attachments/assets/8435ef6f-8152-42fc-85c4-ab3940473379)

![image](https://github.com/user-attachments/assets/3b454b9a-6c88-435f-b543-962f710b3f86)

see the results

![image](https://github.com/user-attachments/assets/adb4c7f2-70d5-4a85-903a-2d64e0ef5cbb)

here Code coverage is 

Coverage
82.7%

![image](https://github.com/user-attachments/assets/f5954fe3-2c85-4283-a736-0bc58308687d)

NOTE:: Coverage is greater than or equal to 80.0%, this should be maintained minimum % every project

NOTE:::Duplicated Lines (%) is less than or equal to 3.0%



Create My own Quality Gates::
=======================

Go to Dashboard click on Quality Gates

![image](https://github.com/user-attachments/assets/b7e1b1c1-e25e-4bf4-acb2-7d3f386df80c)

at left side we can see create & just click on it

![image](https://github.com/user-attachments/assets/b203f151-0ab2-4de3-84f8-a262f462a9c5)


Provide the Name & Click Create


![image](https://github.com/user-attachments/assets/a008a297-54ef-49b3-b5bf-a7df05d19c96)


Your own quality gates are created

![image](https://github.com/user-attachments/assets/f46d3c2a-dfa7-408b-a30d-5d1688de1891)

this is your own quality gates

![image](https://github.com/user-attachments/assets/dab980c2-3767-4d6b-867a-03b423593323)

nditions on New Code
Metric
Operator
Value
Issues
is greater than
0
Security Hotspots Reviewed
is less than
100%
Coverage
is less than
80.0%


Duplicated Lines (%)
is greater than


select your project

![image](https://github.com/user-attachments/assets/3f0aed8a-ebd7-4a27-8e13-4b7bbac978e1)

apply the Grant permissions to a user or a group

![image](https://github.com/user-attachments/assets/a098832f-e4eb-476d-9cbf-e9bbd0a356c5)


Apply all the permissions & click Add

![image](https://github.com/user-attachments/assets/77ce722c-f751-4a9f-844f-edeb677ccb01)

![image](https://github.com/user-attachments/assets/48485193-39d4-4e32-a7cb-c943d0d00ed6)

![image](https://github.com/user-attachments/assets/0b988e9d-df3a-4118-98b8-f4b0cd6e3262)


Create my own Quality Profile::
================================

go to Quality Profiles


![image](https://github.com/user-attachments/assets/9f3c55e8-566a-4f48-8dff-1e473ab0aee0)

select Language

![image](https://github.com/user-attachments/assets/44cc17f2-03f4-4ea0-83ff-8d97a36e1f2b)

total java Rules 527

![image](https://github.com/user-attachments/assets/40ff10ed-e1cf-4ccf-bd80-f9ff509a6ae4)


at right saide top click create

![image](https://github.com/user-attachments/assets/e786de8b-915f-466c-904f-7453eab9efab)

provide the Language & Name and click Create

![image](https://github.com/user-attachments/assets/1a2aaba8-1855-4f13-859e-3cc0b5f0367f)


your own profile

![image](https://github.com/user-attachments/assets/12c55b42-aa02-46c9-a31d-60b46d682e7e)

click Active More rules

![image](https://github.com/user-attachments/assets/d9f3dde5-92cd-466f-9d68-b4bbaae336d5)

Bulk Change

![image](https://github.com/user-attachments/assets/8e927220-c993-4b8f-8ca7-6d9884aa41c4)

Activate In Spring-pipeline project

![image](https://github.com/user-attachments/assets/55e0b2e6-7c53-4b98-b2ce-87f75f935246)

Sure Apply

![image](https://github.com/user-attachments/assets/637731b5-bcbe-4798-b87b-ca808f39f2c1)

Succcessfully Applied my own quality profile rules

Activate In Quality Profile (683 rules)

![image](https://github.com/user-attachments/assets/b530b33a-c75f-470e-9118-e0d49bcbfb96)

Now we are successfully onboarded spring-petclininc project to Sonarqube server

![image](https://github.com/user-attachments/assets/1d8bbf77-c70d-479a-8057-ff62984f23f7)

![image](https://github.com/user-attachments/assets/0c1ea5e5-fd03-46b3-aa51-0f283095ffa8)

![image](https://github.com/user-attachments/assets/45b7263c-0e82-45ff-b06f-915a2af9b464)


Running the Pipeline Once the pipeline is configured, Jenkins will execute the SonarQube analysis during the build process. After the build completes, you can view the analysis results in your SonarQube dashboard.



Code coverage Code smells Bugs Vulnerabilities Duplications These reports will be available in the SonarQube dashboard for your project.




03/06/2025::
==============

Jfrog Artifactory Overview::
======================

JFrog Artifactory is a universal artifact repository manager that serves as a central hub for storing, managing, and distributing software artifacts, binaries, packages, and other assets throughout the software development lifecycle, improving automation, and ensuring release integrity.

Artifact Repository Management:

Allows for storing binaries and artifacts (e.g., libraries, packages, Docker images) in a centralized location.
Supports all major package types (e.g., Maven, Gradle, npm, NuGet, RubyGems, etc.).
Version Control:

Helps in managing versions of your artifacts and ensures the correct version is used during builds and deployments.
Integration with CI/CD:

Integrates seamlessly with CI/CD tools like Jenkins, Bamboo, GitLab CI, and others.
Enables automated publishing of artifacts as part of your continuous integration pipeline.
Access Control & Security:

Provides fine-grained access control and permissions for users and groups.
Supports user authentication, security, and audit trails to ensure compliance and secure artifact management.
Replication:

Allows you to replicate artifacts across multiple Artifactory instances, ensuring high availability and disaster recovery capabilities.
Remote Repositories:

Artifactory can proxy remote repositories, allowing you to cache and fetch external dependencies without re-downloading them each time.
Promotion & Release Management:

You can "promote" artifacts from one repository to another (e.g., from a development repository to a production repository), allowing for better control over releases.
Multi-Platform Support:

Artifactory supports multiple programming languages and platforms, making it a universal solution for managing software dependencies and releases.


Integarte Jfrog with Jenkins::
===========================


![image](https://github.com/user-attachments/assets/ae7344e0-577f-460c-841e-5d9f2a351663)


<img width="846" alt="Jfrog" src="https://github.com/user-attachments/assets/5d07c387-99b9-43e0-97c6-b3b8e008da31" />

First Step:: 

https://jfrog.com/download-jfrog-platform/  ---download url

![image](https://github.com/user-attachments/assets/6ef7f0ee-d89e-4c84-8764-17bcde0c18b3)

previous versions link

https://jfrog.com/download-legacy/?product=artifactory&version=7.104.12

All zip version and search 6.12.1 OSS version

https://releases.jfrog.io/artifactory/bintray-artifactory/


Go to download folder and extract all files 

![image](https://github.com/user-attachments/assets/e7069703-10de-4da6-a435-eb485731d1ca)

go to bin folder

![image](https://github.com/user-attachments/assets/3603144a-46e0-4f5d-96c4-9ddeecafb3f8)

you can found artifactory and go to cmd and run the artifactory.bat from command line

![image](https://github.com/user-attachments/assets/ba5dbde3-6d69-427d-bb06-0aa49038c340)


![image](https://github.com/user-attachments/assets/60310e5b-bdd2-49da-a0ba-e7998f786dd1)

run the artifactory.bat

![image](https://github.com/user-attachments/assets/25f7283b-ebda-40e2-a66f-3b0549994367)

![image](https://github.com/user-attachments/assets/8057d055-c9d5-482d-86d0-d2dca89f6cf8)

once artifactory jfrog up & running navigate to below url default port number is 8081

http://localhost:8081/artifactory

![image](https://github.com/user-attachments/assets/562b1d72-0f16-45c5-9f5f-74fa5ebf4285)


default username & password for jfrog is 

username::: admin

password::: password


04/06/2025::
==============

Jfrog Script::
===============


stage ('Artifactory Server'){

    steps {
    
       rtServer (
       
         id: "Artifactory",
	 
         url: 'http://localhost:8081/artifactory',
	 
         username: 'admin',
	 
          password: 'password',
	  
          bypassProxy: true,
	  
           timeout: 300
                )
    }
}

stage('Upload'){

    steps{
    
        rtUpload (
	
         serverId:"Artifactory" ,
	 
          spec: '''{
	  
           "files": [
	   
              {
	      
              "pattern": "*.war",
	      
              "target": "srinfotech-solutions-private-limited"
	      
              }
                    ]
		    
                   }''',
                )
    }
}

stage ('Publish build info') {

    steps {
    
        rtPublishBuildInfo (
	
            serverId: "Artifactory"
	    
        )
    }
}


installed plugin for artifactory (Jfrog) in Jenkins::
====================================================



![image](https://github.com/user-attachments/assets/542a6be0-9059-4935-9658-81ce27634337)

After installed Artifactory plugin 

Go to Manage Jenkins--System configuration find JFROG

 ![image](https://github.com/user-attachments/assets/5ddbd986-aaee-478b-8a03-e117f53a7b3a)

Click JFrog Platform Instances

![image](https://github.com/user-attachments/assets/c176ad14-5982-4ea3-b960-468d00f851c7)

For user name and password
Go to Jfrogadmin-Securityusers
Default Jfrog U/P----admin/password

![image](https://github.com/user-attachments/assets/83204f3d-bf7b-4bd5-b616-61eaf03ae216)

![image](https://github.com/user-attachments/assets/2af4f08d-5778-4517-8b90-43037eb6ecce)

![image](https://github.com/user-attachments/assets/c104f1c1-6cd0-4911-8eef-b9243a2dd41f)


I need to setup target repository in Jfrog

srinfotech-solutions-private-limited

click Local repository

![image](https://github.com/user-attachments/assets/accda4b3-8ff1-412b-9dfb-c790ff8d9757)


Select maven

![image](https://github.com/user-attachments/assets/a711233f-8298-4fb9-84f7-3acd19d4e73c)

Repository key  :::: srinfotech-solutions-private-limited

![image](https://github.com/user-attachments/assets/a482139b-b0cb-43d6-b5af-17a64a9ea1ef)


Click save and finish

![image](https://github.com/user-attachments/assets/a17b2e49-1e1a-408a-ad16-64cb6bd734b4)

Go to artifacts and check repository is created with name -srinfotech-solutions-private-limited


![image](https://github.com/user-attachments/assets/22ad047d-cf61-4015-bc12-27591d2faf96)



CI/CD all tools ans stages script:: create new job in jenkins and execute below script
======================================================================================



pipeline{

    tools{

        maven 'Maven'
    }
agent any

stages{

    stage('Clone'){

        steps{

            git branch: 'feature/2025.05.27', url: 'https://github.com/srinfotech7358/Petclinic.git'
        }
    }

     stage('Build') {
            steps {
               bat 'mvn clean install'
            }
        }

         stage('Test Cases') {
            steps {
               bat 'mvn test'
            }
        }
 stage('package') {
            steps {
               bat 'mvn package'
            }
        }

         stage('Archive the Artifacts') {
            steps {
               archiveArtifacts artifacts: 'target/*.war', followSymlinks: false
            }
        }
 stage('Sonarqube Analysis') {
            steps {
               
               bat 'mvn package'
              bat '''mvn sonar:sonar \
             -Dsonar.projectKey=spring-petclinic \
             -Dsonar.projectName='spring-petclinic' \
            -Dsonar.host.url=http://localhost:9000 \
            -Dsonar.token=sqp_96cf5222ab632b69c14baa5590210a7125185d5a'''
            }
        }


stage ('Artifactory Server'){
    steps {
       rtServer (
         id: "Artifactory",
         url: 'http://localhost:8081/artifactory',
         username: 'admin',
          password: 'password',
          bypassProxy: true,
           timeout: 300
                )
    }
}

stage('Upload'){
    steps{
        rtUpload (
         serverId:"Artifactory" ,
          spec: '''{
           "files": [
              {
              "pattern": "*.war",
              "target": "srinfotech-solutions-private-limited"
              }
                    ]
                   }''',
                )
    }
}

stage ('Publish build info') {
    steps {
        rtPublishBuildInfo (
            serverId: "Artifactory"
        )
    }
}
 stage('Deploy Application into Tomcat Server') {
            steps {
               deploy adapters: [tomcat9(alternativeDeploymentContext: '', credentialsId: 'NewTomcat', path: '', url: 'http://localhost:8080/')], contextPath: 'SRIN solutions PVT LTD', war: '**/*.war'
            }
        }

}

}



CI/CD::
==========

Continuous Integration & Continutes Deployment & COntinuoues Delivery::
=======================================================================

Continuous Integration(CI)::the practice of automating the integration of code changes from multiple Developers into a single software project. It's a primary DevOps best practice, allowing developers to frequently merge code changes into a central repository,after which automated builds and tests are run automatically.

developers frequently commit to a shared repository using a version control system such as Git,A continuous integration automatically builds and runs unit tests on the new code changes to immediately using jenkins Orchestration.


![image](https://github.com/user-attachments/assets/2713a0f0-ab19-4228-bb6c-2380259ebe7e)


Continuous Deployment(CD) :: Continuous Deployment is an extension of continuous delivery. With continuous deployment, every change that passes through the automated tests and builds is automatically deployed to production without any human intervention. The deployment process is fully automated.

Continuous Delivery (CD)::Continuous Delivery is a software development practice in which code changes are automatically built, tested, and prepared for release to production in a consistent and reliable manner. The key distinction of continuous delivery is that the process of deploying the code to production is done manually by a human decision-maker.


please try to deploy all 3 projects in Tomcat Server 

Project1::

https://github.com/srinfotech7358/devOpsWeb.git

Project2::

https://github.com/srinfotech7358/Petclinic.git


Project3::

https://github.com/srinfotech7358/onlinebookstore.git

Post Deployment 

Spring-petclinic::

![image](https://github.com/user-attachments/assets/811fe50a-25ea-464f-bdaa-ed8a8c7eae52)

onlinebookstore::

![image](https://github.com/user-attachments/assets/21bcb3f2-b95d-4ee7-9f23-b95e479d8b15)


SRInfotech DevOps Project::

![image](https://github.com/user-attachments/assets/f28aa0eb-6be0-485f-8210-4a0557df0df5)



06/06/2025::
============


AWS (Amazon Web Services)::
====================

Amazon Web Services (AWS) is a comprehensive and widely adopted cloud platform offered by Amazon. It provides a broad set of services to help organizations and individuals build and scale applications, manage data, and process workloads in the cloud. AWS is designed to provide flexible, scalable, and cost-effective solutions for computing, storage, networking, machine learning, and much more.

AWS ---Amazon web services

compute services::
Amazon EC2 (Elastic Compute Cloud): Provides scalable virtual servers to run applications.
AWS Lambda: Lets you run code without provisioning or managing servers. It automatically scales based on usage.

Storage services::
Amazon S3 (Simple Storage Service): Object storage for storing and retrieving large amounts of data.
Amazon EBS (Elastic Block Store): Persistent block-level storage for EC2 instances.

Database::
Amazon RDS (Relational Database Service): Managed relational database service supporting multiple database engines (e.g., MySQL, PostgreSQL, MariaDB, etc.).
Amazon DynamoDB: A managed NoSQL database service.
Amazon Aurora: A high-performance relational database engine compatible with MySQL and PostgreSQL.

Network services::
Amazon VPC (Virtual Private Cloud): Lets you create isolated networks within AWS for secure connections.

Security ::

AWS IAM (Identity and Access Management): Controls user access and permissions for AWS resources.
AWS KMS (Key Management Service): Managed service for creating and controlling encryption keys.
Security groups ---inbound, outbould roles


Containers & kuberneties::
ECS  ---elastic containers servcies
EKS  ----estastic kuberneties services
AKS  ---Azure kuberneties services

Cloud watch --Metrics Monitoring

CloudWatch Metrics allows you to track the performance and utilization of AWS resources such as EC2 instances, RDS databases, Lambda functions, S3 buckets, and much more.
These metrics include CPU utilization, disk activity, network traffic, and others. You can create custom metrics for your applications or services as well.

cloud trail ---Security Monitoring:

Use CloudTrail logs to detect unauthorized access or activity in your AWS environment. You can track changes in security settings, unauthorized API calls, or unexpected configuration changes.

Developer Tools::
AWS CodeCommit: Source control service for managing your code repositories.
AWS CodeDeploy: Automates code deployments to EC2 instances and Lambda.
AWS CodePipeline: Continuous integration and continuous delivery (CI/CD) service for automating the release pipeline.




09/06/2025
==========================

AWS EC2 ::
===========
Amazon Elastic Compute Cloud (Amazon EC2) is one of the core services provided by Amazon Web Services (AWS)

Wide Variety of Instance Types:

EC2 instances are grouped into families based on the type of workload they are optimized for. Some common instance families include:
General Purpose: e.g., t3, m5 instances (balanced CPU, memory, and networking).
Compute Optimized: e.g., c5 instances (great for high-performance computing tasks).
Memory Optimized: e.g., r5, x1e instances (designed for high-memory workloads like databases).

create EC2 Ubuntu Linux Machine in AWS::
==================================

Go to AWS ans Search EC2

![image](https://github.com/user-attachments/assets/32cf433a-97b3-444f-9231-1c4aa1da6f79)

Click EC2

![image](https://github.com/user-attachments/assets/f54992d2-7d2b-4a1c-8395-ba5aee7d5899)

Go to instances at left side bar

![image](https://github.com/user-attachments/assets/fcaee5fc-c31a-40cd-a7da-0255afef4373)

Click Launch Instances, EC2  ---> Instances  -----> Launch an instance

![image](https://github.com/user-attachments/assets/9b6128c5-cf0e-48ee-bc11-93852cc3e166)

Select Ubuntu

![image](https://github.com/user-attachments/assets/f610aae5-e7a9-43f6-af7e-e16b6ce9becb)

Select Amazon Machine Image (AMI)

![image](https://github.com/user-attachments/assets/2e5e91a6-cd80-445b-9932-b9d760475be7)


select Instance type,t2 medium

![image](https://github.com/user-attachments/assets/47d6a619-cbe2-41d4-b2ca-40ae44988efb)


Create Create new key pair and provide key pair name

![image](https://github.com/user-attachments/assets/1526a72d-ba98-45be-8998-2d67788c73ef)

click create pair

![image](https://github.com/user-attachments/assets/66a6f77c-36b3-49d3-87a5-abe0358a3c3b)

click launch instance

![image](https://github.com/user-attachments/assets/dca82f59-824d-4cf2-9bf2-ffe81948993c)

instance will be created

![image](https://github.com/user-attachments/assets/ed110a9c-d118-4a08-b678-a3cf945ef5c7)



![image](https://github.com/user-attachments/assets/38ccd3b2-71ce-4102-a047-db937ab13080)

Master & Node communication Via SSH keys::
================================

i have to create 2 EC2 ubuntu machines in AWS
1. Jenkinsmaster
2. Node

![image](https://github.com/user-attachments/assets/9fb55c6b-b0b5-4308-8061-91a23184b6db)


we have already .pem file dowloaded in you local machin

right click from .pem and click Open git bash here option
Now Go to AWS Ubuntu machine which is already created in AWS insatnces and select master machine

![image](https://github.com/user-attachments/assets/ae110666-3e1d-4a48-bfb4-ecb3790187f8)

Click Connect

![image](https://github.com/user-attachments/assets/4130c330-b01d-4a7c-b820-7b836db556b9)

Click SSH Client

![image](https://github.com/user-attachments/assets/fb0dfc0d-abbe-427c-a79b-a10df2f2410c)

Copy URL

>ssh -i "Newkeysmasternode.pem" ubuntu@ec2-18-237-178-192.us-west-2.compute.amazonaws.com

![image](https://github.com/user-attachments/assets/a0bf53d1-3b1a-42a0-8c40-8cb39f85cd09)

Now past that url in Gitbash

![image](https://github.com/user-attachments/assets/e52355e5-73b3-4d7b-9e04-3ce8cd72ffe5)

switch to root user below command run
>Sudo -i

![image](https://github.com/user-attachments/assets/98086ebc-bbd6-4757-ac12-923a2a6eb896)

update the all packages ,please run below command

>sudo apt-get update

![image](https://github.com/user-attachments/assets/3b291e76-4a2a-4d5a-bbd2-58231282e4b7)

Install JDK & Maven:;
============

JDK link

https://bluevps.com/blog/how-to-install-java-on-ubuntu

MAven link

https://phoenixnap.com/kb/install-maven-on-ubuntu



>sudo apt-get install maven
>java -version
>mvn -v

Set java home environment 

>sudo vi /etc/environment
JAVA_HOME=”/usr/lib/jvm/java-8-openjdk-amd64/jre”
MAVEN_HOME=”/usr/share/maven”

Reload your system environment
>source /etc/environment

Veriy the variables was set correctly
>echo $JAVA_HOME
>echo $MAVEN_HOME

Insatll Jenkins on master machine::
====================================

https://phoenixnap.com/kb/install-jenkins-ubuntu

Once installed Jenkins successfully
>we need to enabled the Inbounds and outbounds rules in AWS security groups

Inbounds rules

![image](https://github.com/user-attachments/assets/b7075d75-dd60-42d4-a282-7be861252685)

Copy public IP address and go to browser
Access Jenkins using Public IP address
http://35.86.160.156:8080/

bydefault Jenkins runs on port 8080
Jenkins home path/var/lib/Jenkins
