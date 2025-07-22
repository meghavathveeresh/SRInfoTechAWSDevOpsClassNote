

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



10/06/2025::
===============


![image](https://github.com/user-attachments/assets/a9ba4129-9506-4c2a-9486-0e9905f61253)


AWS any machines default password authentication is disabled , 
we need to enabled in any linux machines
>sudo vi /etc/ssh/sshd_config
>sudo service sshd restart
In EC2 – by default password based authentication is disabled so we need to enabled
>vi /etc/ssh/sshd_config
passwordauthentication :yes

![image](https://github.com/user-attachments/assets/99decb00-3ef0-4528-8e58-0d69bf14ce36)

In ubuntu machine default user is not sudo user,
>visudo

Jenkins ALL=(ALL:ALL) NOPASSWD:ALL

![image](https://github.com/user-attachments/assets/319918d1-2f7c-4878-adcf-d67473e38f36)


>su Jenkins

Switching to new user

![image](https://github.com/user-attachments/assets/86bc74b0-e31f-44aa-bcab-875ed9a3a016)

![image](https://github.com/user-attachments/assets/98b96a48-2ee3-466c-b917-26c1919b15f6)

Once installed Jenkins successfully
>we need to enabled the Inbounds and outbounds rules in AWS security groups

Inbounds rules

![image](https://github.com/user-attachments/assets/b7075d75-dd60-42d4-a282-7be861252685)

Copy public IP address and go to browser
Access Jenkins using Public IP address
http://35.86.160.156:8080/

bydefault Jenkins runs on port 8080
Jenkins home path/var/lib/Jenkins

Now Go to Node Machine::
==============
Please insatll JDK & Maven in node machine and setup environemnt varibles

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

comminicate master & node via SSH keys
>ssh-keygen -t ed25519
after generated the keys, we need to  copy public key to node machine

option-1 to copy keys from master to node
>ssh-copy-id user@ipaddressofnodemachine
>ssh-copy-id node@172.31.44.169

2nd option --copy keys manually from master to node

3rd options --i have created authorized_keys  file in node machine and copy public key from master to node

keys copied correcctly try below command to run,

Syntax::
=============

>ssh username@ipaddressofNodeMachine

>ssh node1@ip-172-31-11-212.us-west-2.compute.internal



NODE::
-------

1. we need to create .ssh directory
>mkdir .ssh/
>cd .ssh/
>touch authorized_keys
>ls

here i want copy public key from master to node machine into the authorized_keys file

please restsrt all the machines

i want call node1 machine fomr jenkins master

>ssh usernameofnode@ipaddressofnodemachine

>jenkins@ip-172-31-36-36:~/.ssh$ ssh node1@ip-172-31-41-243


Master Node Configuration::
>got to manage Jenkins
>manage Nodes

>click new node
Remote root directory

![image](https://github.com/user-attachments/assets/774c7270-0607-4332-8679-ebad4a459979)

![image](https://github.com/user-attachments/assets/55da9a7b-3178-47cf-be6d-72b452a59b2d)

Launch methods via ssh

![image](https://github.com/user-attachments/assets/aa7e51ac-278f-473c-9512-bfb35422fea8)


Add credentials

![image](https://github.com/user-attachments/assets/2a3ae243-9a58-4666-bacd-317298d68f33)

>Host Key Verification Strategy
![image](https://github.com/user-attachments/assets/a926aed1-85d6-42e1-804f-da5df9792eed)

Master Node Configuration::
>got to manage Jenkins
>manage Nodes
>click new node
Remote root directory

![image](https://github.com/user-attachments/assets/190f9e24-2842-4462-9773-6c98c7980d77)

![image](https://github.com/user-attachments/assets/10dcf0c4-7088-4071-a6e0-8f4729603029)
 
 

Launch methods via ssh

 ![image](https://github.com/user-attachments/assets/f25a3610-8d32-43ca-bde3-644426d37cb1)


Add credentials ::

option-1::
=========

this time please use credentials option SSH key with private key from node machine

option::2 
===========
please use credentials with Username & password and let's try if you copy properly ,agent machine will conenct Successfully

 ![image](https://github.com/user-attachments/assets/d54e7393-a5b9-4194-8f50-c206b02c39d1)

 ![image](https://github.com/user-attachments/assets/2113f8d7-18d1-4e66-84ec-267c05fde9b5)

>Host Key Verification Strategy

 ![image](https://github.com/user-attachments/assets/58a7b48d-eab5-45a7-9661-1a72578ceda5)


Agent successfully connected

![image](https://github.com/user-attachments/assets/823523dc-fe3e-432c-b3d8-9c645483d30a)

 

Execute Jenkins job using slave 
Create one test slave job in Jenkins

>select Restrict where this project can be run

![image](https://github.com/user-attachments/assets/d6c206ac-06a1-4564-9351-7b35e4f4c521)


>select Label Expression

![image](https://github.com/user-attachments/assets/85b8897c-f6ec-4bd2-8bb9-3821251c20da)

please create 2 job in jenkins master and setup 1 job in Node machine and 2nd job master machine, just trigger Build Now 

Please observe below screenshot 2 job running different machines 

![image](https://github.com/user-attachments/assets/94005ac8-cb37-4c97-ba0e-14adf7c71566)

advantage of master & Node Integartion

![image](https://github.com/user-attachments/assets/5551bbab-46b7-49ae-b6c2-093299d2ecb2)

![image](https://github.com/user-attachments/assets/ac59dbc9-c012-44a0-ae98-0fbcc2d4e5d8)



11/06/2025::
==============

Ansible Playbooks Introduction::
==========================

Ansible playbooks are the heart of automation with Ansible. They are simple YAML (Yet Another Markup Language) files that define automation tasks in a structured, human-readable format. Playbooks allow you to automate configurations, deployments, and orchestration tasks in a clear and organized way.


![image](https://github.com/user-attachments/assets/9b2fada9-16f9-49b1-b3bf-d85bd0795e57)



Key Concepts::
==============

Playbook: A playbook is a file that contains one or more "plays." Each play defines a set of tasks to be executed on a group of hosts. The playbook can be used for things like installing packages, managing users, configuring services, etc.

Task: A task is an individual unit of work. Tasks define specific actions, such as installing a package, starting a service, or copying a file. Tasks are executed sequentially, in the order in which they are written in the playbook.

Inventory: An inventory is a list of hosts that Ansible will manage. The inventory file defines which machines to target. An inventory can group hosts together (e.g., web servers, db servers) for easy management.

Modules: Ansible provides numerous modules that are responsible for performing specific tasks like managing packages, services, files, etc. Common modules include apt, yum, service, copy, and file.



Create 3 AWS ubuntu machines::
=================================

1. ACS --ansible control server
2.node1
3.node2


Steps to configure ACS::
===========================

1. passwordauthentication enabled

>sudo vi /etc/ssh/sshd_config

2. Create New user-->ansible and user should be provide the sudo permissions
   
>visudo

ansible ALL=(ALL:ALL) NOPASSWD:ALL

>su ansible
Switching to new user

3.install ansible in Ansible control server

https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-22-04

> ansible --version

4. keybased authentication via SSH keys

   >ssh-keygen -t ed25519

   Generated private and public keys

   5. copy publickey from ansible control server to node machines

   if above steps are configured properly ,it will communications happend via sshkeys

![image](https://github.com/user-attachments/assets/b1b67c08-47b0-4dc3-be5f-d9d5c41d3573)


Steps to configure Node1::
===========================

1. passwordauthentication enabled

>sudo vi /etc/ssh/sshd_config

2. Create New user-->node1 and user should be provide the sudo permissions
   
>visudo

node1 ALL=(ALL:ALL) NOPASSWD:ALL

>su node1
Switching to new user node1

3.install python in node1 machine

https://docs.vultr.com/how-to-install-python-and-pip-on-ubuntu-24-04


> python3 --version

4. keybased authentication via SSH keys



12/06/2025::
==============


Steps to configure Node1::
===========================

1. passwordauthentication enabled

>sudo vi /etc/ssh/sshd_config

2. Create New user-->node2 and user should be provide the sudo permissions
   
>visudo

node2 ALL=(ALL:ALL) NOPASSWD:ALL

>su node1
Switching to new user node2

3.install python in node1 machine

https://docs.vultr.com/how-to-install-python-and-pip-on-ubuntu-24-04


> python3 --version

4. keybased authentication via SSH keys

  if above steps are configured properly ,it will communications happend via sshkeys


all these 3 machine ping to each other and see beow screenshots all 3 machines pings each other

NOTE::
1.please create authorized_keys file in ansible master and copy public key to authorized kesy fiile
2.ssh-copy-id ansible@localhost
Restart machine
>cd /etc/ansible
>ansible -m ping all
It working 
>sudo nano hosts
Add all host names or ipaddress or private DNS names

![image](https://github.com/user-attachments/assets/2c501a8f-240a-4874-aef7-498f549dacd5)


Steps::
======
ubuntu@ip-172-31-28-207:~$ sudo -i

root@ip-172-31-28-207:~# su ansible

ansible@ip-172-31-28-207:/root$ cd ~

ansible@ip-172-31-28-207:~$ cd /etc/ansible/

ansible@ip-172-31-28-207:/etc/ansible$ ansible -m ping all

**node2@ip-172-31-42-167.us-west-2.compute.internal | SUCCESS** => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.12"
    },
    "changed": false,
    "ping": "pong"
}
[WARNING]: Platform linux on host node1@ip-172-31-39-93.us-west-2.compute.internal is using the
discovered Python interpreter at /usr/bin/python3.12, but future installation of another Python
interpreter could change the meaning of that path. See https://docs.ansible.com/ansible-
core/2.18/reference_appendices/interpreter_discovery.html for more information.
**node1@ip-172-31-39-93.us-west-2.compute.internal | SUCCESS** => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.12"
    },
    "changed": false,
    "ping": "pong"
}
[WARNING]: Platform linux on host ansible@localhost is using the discovered Python interpreter at
/usr/bin/python3.12, but future installation of another Python interpreter could change the
meaning of that path. See https://docs.ansible.com/ansible-
core/2.18/reference_appendices/interpreter_discovery.html for more information.
**ansible@localhost | SUCCESS** => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.12"
    },
    "changed": false,
    "ping": "pong"
}
[WARNING]: Platform linux on host ansible@ip-172-31-42-190.us-west-2.compute.internal is using the
discovered Python interpreter at /usr/bin/python3.12, but future installation of another Python
interpreter could change the meaning of that path. See https://docs.ansible.com/ansible-
core/2.18/reference_appendices/interpreter_discovery.html for more information.
**ansible@ip-172-31-42-190.us-west-2.compute.internal** | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.12"
    },
    "changed": false,
    "ping": "pong"
}


all these 3 machine ping to each other and see beow screenshots all 3 machines pings each other

![image](https://github.com/user-attachments/assets/ca010d9c-5746-4421-ac5f-37c88dabe369)



13/06/2025::
===============

Ansible Playbooks Introduction::
==========================

Ansible playbooks are the heart of automation with Ansible. They are simple YAML (Yet Another Markup Language) files that define automation tasks in a structured, human-readable format. Playbooks allow you to automate configurations, deployments, and orchestration tasks in a clear and organized way.

Key Concepts::
==============

Playbook: A playbook is a file that contains one or more "plays." Each play defines a set of tasks to be executed on a group of hosts. The playbook can be used for things like installing packages, managing users, configuring services, etc.

Task: A task is an individual unit of work. Tasks define specific actions, such as installing a package, starting a service, or copying a file. Tasks are executed sequentially, in the order in which they are written in the playbook.

Inventory: An inventory is a list of hosts that Ansible will manage. The inventory file defines which machines to target. An inventory can group hosts together (e.g., web servers, db servers) for easy management.

Modules: Ansible provides numerous modules that are responsible for performing specific tasks like managing packages, services, files, etc. Common modules include apt, yum, service, copy, and file.


Structure of a Basic Playbook:
===============================
A basic playbook has the following components:

YAML Header: The file begins with a --- to indicate it’s a YAML file.

 the hosts (target machines)
 become: yes   ----->Sudo user 

Tasks: Tasks define the actions to be executed on the target systems.

![image](https://github.com/user-attachments/assets/71982463-6b41-4481-af94-29c76690b0b6)

I want to see where the Ansible is installed on ACS
>cd /etc/ansible

NOTE::
==========
Playbook is written in YAML format
Inside the playbook tasks
Each task is a module
Playbook is a one of yaml file
Yaml file is a collection of key-value pairsset of all tasks
Playbook is tell to the ansible what are the tasks can be performed
Each task  one module
Module is a smallest item of ansible
Module can be used to individual or smallest task can be performed
Any configuration management tool should maintain ‘state’


hosts: all (apply all we can be mentioned in inventory )
become: yes  (become user as a sudo user)
tasks:

we can search in google ansible playbook
https://docs.ansible.com/ansible/latest/user_guide/playbooks.html
https://docs.ansible.com/ansible/latest/user_guide/playbooks_intro.html#basics


install git example playbook::
============================== 

installgit.yml
---
- hosts: all

  become: yes
  
  tasks:
  
  -  name: install git
    
     apt:
     
       name: git
     
       state: present
     
       update_cache: yes

     
note:::default state is present 
update_cache: yes tells Ansible to run the apt-get update command on the remote machine before performing any further package operations (like installing or upgrading packages).
become: yes  # Elevate privileges to execute tasks as root



ansible@ip-172-31-19-120:/etc/ansible$ ansible-playbook installgit.yml

PLAY [all] **********************************************************************************************

TASK [Gathering Facts] **********************************************************************************
[WARNING]: Platform linux on host localhost is using the discovered Python interpreter at
/usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of
that path. See https://docs.ansible.com/ansible-
core/2.18/reference_appendices/interpreter_discovery.html for more information.
ok: [localhost]
[WARNING]: Platform linux on host node2@172.31.30.90 is using the discovered Python interpreter at
/usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of
that path. See https://docs.ansible.com/ansible-
core/2.18/reference_appendices/interpreter_discovery.html for more information.
ok: [node2@172.31.30.90]
[WARNING]: Platform linux on host node1@172.31.30.121 is using the discovered Python interpreter at
/usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of
that path. See https://docs.ansible.com/ansible-
core/2.18/reference_appendices/interpreter_discovery.html for more information.
ok: [node1@172.31.30.121]

TASK [install git] **************************************************************************************
ok: [node2@172.31.30.90]
ok: [node1@172.31.30.121]
ok: [localhost]

PLAY RECAP **********************************************************************************************
localhost                  : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
node1@172.31.30.121        : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
node2@172.31.30.90         : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

ansible@ip-172-31-19-120:/etc/ansible$ git --version
git version 2.43.0
ansible@ip-172-31-19-120:/etc/ansible$ Read from remote host ec2-34-226-192-28.compute-1.amazonaws.com: Connection reset by peer
Connection to ec2-34-226-192-28.compute-1.amazonaws.com closed.
client_loop: send disconnect: Connection reset by peer

java and git install playbook::
================================

>sudo vi installgit.yml

copy git & JDK playbook code to installgit.yml


---

- hosts: all
  
  
  become: yes
  
  tasks:
  
  -  name: install git
    
     apt:
     
       name: git
     
       state: present
     
       update_cache: yes

  -  name: Install Java
    
     apt:
     
       name: openjdk-17-jdk
     
       state: present

Run the playbook::
===============
>ansible-planbook <playbookname>
>ansible-playbook installgit.yml

ansible@ip-172-31-42-190:/etc/ansible$ ansible-playbook installgit.yml

PLAY [all] ***********************************************************************************************************

TASK [Gathering Facts] ***********************************************************************************************
[WARNING]: Platform linux on host ansible@localhost is using the discovered Python interpreter at
/usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of that path. See
https://docs.ansible.com/ansible-core/2.18/reference_appendices/interpreter_discovery.html for more information.
ok: [ansible@localhost]
[WARNING]: Platform linux on host node2@ip-172-31-42-167.us-west-2.compute.internal is using the discovered Python
interpreter at /usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of
that path. See https://docs.ansible.com/ansible-core/2.18/reference_appendices/interpreter_discovery.html for more
information.
ok: [node2@ip-172-31-42-167.us-west-2.compute.internal]
[WARNING]: Platform linux on host node1@ip-172-31-39-93.us-west-2.compute.internal is using the discovered Python
interpreter at /usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of
that path. See https://docs.ansible.com/ansible-core/2.18/reference_appendices/interpreter_discovery.html for more
information.
ok: [node1@ip-172-31-39-93.us-west-2.compute.internal]

TASK [install git in ubuntu machines] ********************************************************************************
ok: [node1@ip-172-31-39-93.us-west-2.compute.internal]
ok: [node2@ip-172-31-42-167.us-west-2.compute.internal]
ok: [ansible@localhost]

TASK [install JDK17 in ubuntu machines] ******************************************************************************
changed: [node2@ip-172-31-42-167.us-west-2.compute.internal]
changed: [ansible@localhost]
changed: [node1@ip-172-31-39-93.us-west-2.compute.internal]

PLAY RECAP ***********************************************************************************************************
ansible@localhost          : ok=3    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
node1@ip-172-31-39-93.us-west-2.compute.internal : ok=3    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
node2@ip-172-31-42-167.us-west-2.compute.internal : ok=3    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

ansible@ip-172-31-42-190:/etc/ansible$ java --version
openjdk 17.0.15 2025-04-15
OpenJDK Runtime Environment (build 17.0.15+6-Ubuntu-0ubuntu124.04)
OpenJDK 64-Bit Server VM (build 17.0.15+6-Ubuntu-0ubuntu124.04, mixed mode, sharing)

Usefull Google links::
===========

https://docs.ansible.com/ansible/2.9/modules/list_of_all_modules.html
https://docs.ansible.com/ansible/2.9/modules/apt_module.html#parameters
https://www.geeksforgeeks.org/how-to-install-java-using-ansible-playbook/
https://www.yamllint.com/
https://www.geeksforgeeks.org/how-to-install-tomcat-using-ansible-playbook/

Ansible all modules links::
=========================

https://docs.ansible.com/ansible/latest/modules/list_of_all_modules.html
https://docs.ansible.com/ansible/2.9/modules/list_of_all_modules.html



i want to insatll 4 spfwares(git,jdk17,tree & apache2) :: below playbook name -----> softwaresinstallition.yml
====================================================================================================

created playbook for this requirement

---
- hosts: all

  become: yes

  tasks:

  -  name: install git in ubuntu machines

       apt:

       name: git
     
       state: present
     
       update_cache: yes

   -  name: install JDK17 in ubuntu machines
     
     apt:
  
       name: openjdk-17-jdk
  
       state: absent

   -  name: install tree in ubuntu machines

      apt:
      
       name: tree
      
       state: present

  -  name: install apache2 in ubuntu machines
 
     apt:
 
       name: apache2
     
       state: absent
     

>ansible-playbook softwaresinstallition.yml


LAB Practice::
===============

ansible@ip-172-31-42-190:/etc/ansible$ sudo vi softwaresinstallition.yml
ansible@ip-172-31-42-190:/etc/ansible$ ansible-playbook softwaresinstallition.yml

PLAY [all] ***********************************************************************************************************

TASK [Gathering Facts] ***********************************************************************************************
[WARNING]: Platform linux on host ansible@localhost is using the discovered Python interpreter at
/usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of that path. See
https://docs.ansible.com/ansible-core/2.18/reference_appendices/interpreter_discovery.html for more information.
ok: [ansible@localhost]
[WARNING]: Platform linux on host node1@ip-172-31-39-93.us-west-2.compute.internal is using the discovered Python
interpreter at /usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of
that path. See https://docs.ansible.com/ansible-core/2.18/reference_appendices/interpreter_discovery.html for more
information.
ok: [node1@ip-172-31-39-93.us-west-2.compute.internal]
[WARNING]: Platform linux on host node2@ip-172-31-42-167.us-west-2.compute.internal is using the discovered Python
interpreter at /usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of
that path. See https://docs.ansible.com/ansible-core/2.18/reference_appendices/interpreter_discovery.html for more
information.
ok: [node2@ip-172-31-42-167.us-west-2.compute.internal]

TASK [install git in ubuntu machines] ********************************************************************************
ok: [node1@ip-172-31-39-93.us-west-2.compute.internal]
ok: [node2@ip-172-31-42-167.us-west-2.compute.internal]
ok: [ansible@localhost]

TASK [install JDK17 in ubuntu machines] ******************************************************************************
ok: [ansible@localhost]
changed: [node2@ip-172-31-42-167.us-west-2.compute.internal]
changed: [node1@ip-172-31-39-93.us-west-2.compute.internal]

TASK [install tree in ubuntu machines] *******************************************************************************
ok: [ansible@localhost]
changed: [node2@ip-172-31-42-167.us-west-2.compute.internal]
changed: [node1@ip-172-31-39-93.us-west-2.compute.internal]

TASK [install apache2 in ubuntu machines] ****************************************************************************
changed: [node1@ip-172-31-39-93.us-west-2.compute.internal]
changed: [node2@ip-172-31-42-167.us-west-2.compute.internal]
changed: [ansible@localhost]

PLAY RECAP ***********************************************************************************************************
ansible@localhost          : ok=5    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
node1@ip-172-31-39-93.us-west-2.compute.internal : ok=5    changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
node2@ip-172-31-42-167.us-west-2.compute.internal : ok=5    changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0


Please enabled Inbound and Outbound rules::
=======================================

Inbound and outbound rules refer to the types of network traffic that are allowed or denied to and from a system, such as a server, virtual machine, or network device. These rules are typically defined in firewalls or security groups (such as in cloud environments like AWS, Azure, or Google Cloud). The primary goal is to control which data can enter or leave a network, ensuring security and proper access control.

Here’s a detailed explanation of inbound and outbound rules:

 Inbound Rules::
Inbound rules control traffic entering a system or network. These rules define which types of external traffic are allowed to reach a server, instance, or device.

Common Uses:
Allowing specific users or services to access the system.

Restricting access to the system from unauthorized users.

Opening ports for services like web servers (HTTP, HTTPS), SSH, database connections, etc

Allowing incoming traffic on port 80 (HTTP) so that users can access a web server.

Outbound Rules::
Outbound rules control traffic leaving a system or network. These rules define which traffic is allowed to exit a server or device and reach external destinations.

Common Uses:
Allowing a server to access external services like APIs, databases, or external servers.

Restricting unwanted traffic from the system to external destinations.

Controlling the flow of outgoing traffic to ensure compliance with security policies.

Allow HTTP/HTTPS: Allow outbound traffic on ports 80 (HTTP) and 443 (HTTPS) to any IP:



![image](https://github.com/user-attachments/assets/76772963-84d4-4515-99f6-7fc74fd05e5b)


After execute the playbook see the Apache2 in browser

http://publicIPaddress

http://44.247.80.104/

ACS----Ansible control server

![image](https://github.com/user-attachments/assets/9f8a2ebb-fd45-4d59-a187-4c91a9e72367)


NODE1::

![image](https://github.com/user-attachments/assets/df4b3dd4-ee4a-48f6-85b2-8a1b541e46de)

NODE2::

![image](https://github.com/user-attachments/assets/60e75d37-a96c-4fb4-b8c1-aa1ca52f8867)





17/06/2025::
=================


Executing ansible in 2 ways
1.	Adhoc command  ---> yearly base
2.	Playbook (YAML/YML) format --> use for repetitive work

Inventory::
==========
where hosts/ipaddress are stored

I want to create my own inventory

>Cd /etc/ansible

![image](https://github.com/user-attachments/assets/e03cd989-34e8-46f5-88d0-9af56f11b6d9)

![image](https://github.com/user-attachments/assets/7a4d1993-1c1e-4da6-94b0-eeb105cb0d36)

![image](https://github.com/user-attachments/assets/79f8fb33-19d1-47a9-b26e-aff30d75d408)

>cat /etc/ansible/hosts

Sudo vi hosts

Copy all hosts

![image](https://github.com/user-attachments/assets/bcda07ba-ab66-4b86-bf67-f7ad9c556230)

I want categories into Inventory groups::
===================================

In Ansible, inventory groups are used to organize and categorize hosts (machines or servers) into logical groups. This allows you to apply tasks to specific sets of servers, simplifying playbook management and execution. An inventory is a list of managed hosts and their associated metadata, and groups are one of the key components of that structure.

Here’s a detailed explanation of Ansible inventory groups

1. What Are Inventory Groups?
An inventory group in Ansible is a way to group hosts based on a shared characteristic. For example, you might have groups for different environments (e.g., dev, prod), different types of servers (e.g., web_servers, db_servers), or other logical categories that fit your needs.

static inventory groups defined in the standard INI or YAML format.

# Define groups of hosts:: >sudo vi hosts

[web_servers]

 ansiblenode1@172.31.20.135
 
 ansiblenode2@172.31.30.200
 
 localhost
 
[db_servers]

ansiblenode1@172.31.20.135

ansiblenode2@172.31.30.200

[app_servers]

 localhost
 
i want to insatll 3 spfwares :: below playbook name -----> installsoftware.yml
==============================

---
- hosts: web_server
  
  become: yes
  
  tasks:
  
  -  name: install git
    
     apt:
     
       name: git
     
       state: present
     
       update_cache: yes

  -  name: install tree
    
     apt:
     
       name: tree
     
       state: present  

  -  name: install apache
  
     apt:
     
       name: apache2
     
       state: present

once above two files created run the below command

>ansible-playbook -i hosts installsoftware.yml
     
![image](https://github.com/user-attachments/assets/36d33a9a-b113-402c-80f7-1e9c404a245b)

>ansible -i hosts -m ping Webserver

Best practice is you need to create our own inventories

>sudo vi hosts

after ran the above yaml, please try to access all machines with IPaddresss

![image](https://github.com/user-attachments/assets/4a7778cd-6b97-4822-ad5e-11bbdde82231)

![image](https://github.com/user-attachments/assets/96a67d2a-993a-47ff-aa79-3dc8cd7aa06a)

![image](https://github.com/user-attachments/assets/01ee5e45-446e-42f2-a47f-c8b3e2fbe2f5)

Please enabled Inbound and Outbound rules::
=======================================

Inbound and outbound rules refer to the types of network traffic that are allowed or denied to and from a system, such as a server, virtual machine, or network device. These rules are typically defined in firewalls or security groups (such as in cloud environments like AWS, Azure, or Google Cloud). The primary goal is to control which data can enter or leave a network, ensuring security and proper access control.

Here’s a detailed explanation of inbound and outbound rules:

 Inbound Rules::
Inbound rules control traffic entering a system or network. These rules define which types of external traffic are allowed to reach a server, instance, or device.

Common Uses:
Allowing specific users or services to access the system.

Restricting access to the system from unauthorized users.

Opening ports for services like web servers (HTTP, HTTPS), SSH, database connections, etc

Allowing incoming traffic on port 80 (HTTP) so that users can access a web server.

Outbound Rules::
Outbound rules control traffic leaving a system or network. These rules define which traffic is allowed to exit a server or device and reach external destinations.

Common Uses:
Allowing a server to access external services like APIs, databases, or external servers.

Restricting unwanted traffic from the system to external destinations.

Controlling the flow of outgoing traffic to ensure compliance with security policies.

Allow HTTP/HTTPS: Allow outbound traffic on ports 80 (HTTP) and 443 (HTTPS) to any IP:



![image](https://github.com/user-attachments/assets/0e51f799-d746-45a5-94cb-f358ade65ba2)

![image](https://github.com/user-attachments/assets/8fa024b7-0999-40f7-94cb-3eaa018fbd41)

![image](https://github.com/user-attachments/assets/2ca3de47-8bea-4f5a-a35e-0238788cb7c7)


Install LAMP on ubuntu 24.04::
==================================

A LAMP stack stands for Linux, Apache, MySQL, and PHP, which is a popular open-source software stack used for web development. It provides everything you need to set up a dynamic website or web application.

Here’s a quick overview of each component:

Linux: The operating system (in this case, Ubuntu).

Apache: The web server that serves your website’s files.

MySQL: The database management system for storing and retrieving data.

PHP: The programming language used for dynamic web page generation.



Manual Steps::
====================

https://www.digitalocean.com/community/tutorials/how-to-install-lamp-stack-on-ubuntu

>sudo apt update

>sudo apt install apache2

>sudo apt install mysql-server

>sudo apt install php

>sudo apt install libapache2-mod-php

>sudo apt install php-mysql

>sudo systemctl restart apache2

>sudo apt install php-cli

>sudo nano /var/www/html/info.php

above steps are manually installed all required softwares in LAMP project but my requirement is to write a Playbook for those manuall steps

Playbook for LAMP::  phppackage.yml
=====================



---
- hosts: all

  become: yes

  tasks:
  
  -  name: install apache2

     apt:

     name: apache2

     state: present

     update_cache: yes

  -  name: install php

      apt:

      name: php

      state: present  

  -  name: install mysql-server

     apt:

      name: mysql-server

      state: present
     
  -  name: install libapache2-mod-php

     apt:

     name: libapache2-mod-php

     state: present
                   
  -  name: install  php-mysql

     apt:

     name: php-mysql

     state: present
     
  -  name: restart apache

     service:

     name: apache2

      enabled: true

     state: restarted

  -  name: install php-cli

     apt:

     name: php-cli

      state: present 

  -  name: copy module info.php

     copy:

     src: info.php

     dest: /var/www/html/info.php     


Copy Module::
=========

https://docs.ansible.com/ansible/latest/collections/ansible/builtin/copy_module.html

Service Module::
==================

https://docs.ansible.com/ansible/latest/collections/ansible/builtin/service_module.html

info.php ::
==========

https://www.digitalocean.com/community/tutorials/how-to-install-lamp-stack-on-ubuntu



hosts grouping:
================

![image](https://github.com/user-attachments/assets/2eb4e4d2-bda2-44fa-8e86-d4b5bd51ed9e)


[Webservers]
ansiblenode1@172.31.20.135
ansiblenode2@172.31.30.200
localhost

[Appservers]
ansiblenode1@172.31.20.135

[DBservers]

localhost


Reference flow::
==============
ansible@ip-172-31-28-207:/etc/ansible/playbook$ ls
hosts  info.php  installsoftwares.yml  phppackage.yml
ansible@ip-172-31-28-207:/etc/ansible/playbook$ sudo vi phppackage.yml
ansible@ip-172-31-28-207:/etc/ansible/playbook$ sudo vi hosts
ansible@ip-172-31-28-207:/etc/ansible/playbook$ sudo vi phppackage.yml
ansible@ip-172-31-28-207:/etc/ansible/playbook$ ansible-playbook -i hosts phppackage.yml
ansible@ip-172-31-28-207:/etc/ansible/playbook$ sudo vi info.php
ansible@ip-172-31-28-207:/etc/ansible/playbook$ ansible-playbook -i hosts phppackage.yml

PLAY [Webservers] *********************************************************************************************

TASK [Gathering Facts] ****************************************************************************************
[WARNING]: Platform linux on host localhost is using the discovered Python interpreter at /usr/bin/python3.12,
but future installation of another Python interpreter could change the meaning of that path. See
https://docs.ansible.com/ansible-core/2.17/reference_appendices/interpreter_discovery.html for more
information.
ok: [localhost]
[WARNING]: Platform linux on host ansiblenode2@172.31.30.200 is using the discovered Python interpreter at
/usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of that
path. See https://docs.ansible.com/ansible-core/2.17/reference_appendices/interpreter_discovery.html for more
information.
ok: [ansiblenode2@172.31.30.200]
[WARNING]: Platform linux on host ansiblenode1@172.31.20.135 is using the discovered Python interpreter at
/usr/bin/python3.12, but future installation of another Python interpreter could change the meaning of that
path. See https://docs.ansible.com/ansible-core/2.17/reference_appendices/interpreter_discovery.html for more
information.
ok: [ansiblenode1@172.31.20.135]

TASK [install apache2] ****************************************************************************************
ok: [ansiblenode2@172.31.30.200]
ok: [ansiblenode1@172.31.20.135]
ok: [localhost]

TASK [install php] ********************************************************************************************
ok: [ansiblenode1@172.31.20.135]
ok: [ansiblenode2@172.31.30.200]
ok: [localhost]

TASK [install mysql-server] ***********************************************************************************
ok: [ansiblenode1@172.31.20.135]
ok: [ansiblenode2@172.31.30.200]
ok: [localhost]

TASK [install libapache2-mod-php] *****************************************************************************
ok: [ansiblenode1@172.31.20.135]
ok: [ansiblenode2@172.31.30.200]
ok: [localhost]

TASK [install  php-mysql] *************************************************************************************
ok: [ansiblenode1@172.31.20.135]
ok: [ansiblenode2@172.31.30.200]
ok: [localhost]

TASK [restart apache] *****************************************************************************************
changed: [ansiblenode2@172.31.30.200]
changed: [localhost]
changed: [ansiblenode1@172.31.20.135]

TASK [install php-cli] ****************************************************************************************
ok: [ansiblenode1@172.31.20.135]
ok: [localhost]
ok: [ansiblenode2@172.31.30.200]

TASK [copy module info.php] ***********************************************************************************
changed: [localhost]
changed: [ansiblenode2@172.31.30.200]
changed: [ansiblenode1@172.31.20.135]

PLAY RECAP ****************************************************************************************************
ansiblenode1@172.31.20.135 : ok=9    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
ansiblenode2@172.31.30.200 : ok=9    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
localhost                  : ok=9    changed=2    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0



Please execute above steps we will see the php insatlled on all 3 machines

![image](https://github.com/user-attachments/assets/d49aa2d0-69ad-4c40-8408-2ccf3edbf838)

![image](https://github.com/user-attachments/assets/74b9e6dd-8fb1-452f-85f1-faffd48d7dae)

![image](https://github.com/user-attachments/assets/6d58255a-e6ea-44b7-a4e2-39f8598358b3)


info.php::
===========

<?php
phpinfo();
?>




Working Script::
====================

---
- hosts: Webservers
  become: yes
  tasks:
  -  name: install Apache2 in ubuntu machines
     apt:
       name: apache2
       state: present
  -  name: apache2 started in ubuntu machines
     service:
       name: apache2
       enabled: yes
       state: started
  -  name: apache2 enabled in ubuntu machines
     service:
       name: apache2
       enabled: yes
       state: enabled
  -  name: install php php-fpm in ubuntu machines
     apt:
       name: php php-fpm
       state: present
  -  name: install php-mysql in ubuntu machines
     apt:
       name: php-mysql
       state: present
  -  name: install php-opcache in ubuntu machines
     apt:
       name: php-opcache
       state: present          
  -  name: install php-cli in ubuntu machines
     apt:
       name: php-cli
       state: present
  -  name: install libapache2-mod-php in ubuntu machines
     apt:
       name: libapache2-mod-php
       state: present
  -  name: Copy info.php file to Destination folder
     copy:
       src: info.php
       dest: /var/www/html/info.php



18/06/2025::
=================

How do i write a loops In Ansible::
=======================================

https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_loops.html

Repeated tasks can be written as standard loops over a simple list of strings. You can define the list directly in the task.

Using loops Examples::

- name: Add several users
  ansible.builtin.user:
    name: "{{ item }}"
    state: present
    groups: "wheel"
  loop:
     - testuser1
     - testuser2


ansible loops
===================

Working Script and Please try to execute below scripts using Ansible Loops::

---
- hosts: Websevers
  become: yes
  tasks:

  -  name: install all php packages in ubuntu machines
     apt:
       name: "{{ item }}"
       state: present
     loop:
       - php-fpm
       - php-mysql
       - php-opcache
       - php-cli
       - libapache2-mod-php
       - apache2
  -  name: apache2 started in ubuntu machines
     service:
       name: apache2
       enabled: yes
       state: started
  -  name: apache2 enabled in ubuntu machines
     service:
       name: apache2
       enabled: yes
       state: reloaded     
  -  name: apache2 restarted in ubuntu machines
     service:
       name: apache2
       enabled: yes
       state: restarted
  -  name: Copy info.php file to Destination folder
     copy:
       src: info.php
       dest: /var/www/html/info.php




     19/06/2025::
     ==================


Setup module in ansible::
==========================

Setup module is used to collect the facts

Facts-----> information gather from nodes called facts

>ansible -I hosts -m setup Webserver

![image](https://github.com/user-attachments/assets/c6325665-4a15-400a-8240-bff439426f43)

Using filter command::
=========================

If you're asking about the "filter" parameter in Ansible's command-line modules like below


>ansible -i hosts -m setup -a "filter=*os*" Webserver

ansible_os_family": "Debian"

Ansible when statements

https://docs.ansible.com/ansible/latest/user_guide/playbooks_conditionals.html#the-when-statement


ansible_os_family": "Debian"

When condition is always used bottom of the script and using scrips we can able to run a playbook on a different platforms 

1.Debian
2.Redhat
---
- hosts: Webserver

  become: yes

  tasks:
  - name: install apache

    apt:
      name: apache2

    state: present

    update_cache: yes

    when: ansible_os_family == "Debian"  
  - name: install apache

    yum:

    name: httpd

     state: present

    when: ansible_os_family == "Redhat"


In Ansible, variables are used to store values that can be referenced and used throughout your playbooks, roles, and tasks. This allows for dynamic, reusable, and flexible automation. Here’s a basic breakdown of how Ansible variables work and the different ways you can define and use them:


define variables in 3 places
1.	Inventory level  lowest priority
2.	Playbook level 
3.	Command line level –highest level priority


defined variable in Ansible::
 
 1.commandline level  ---highest priorty 
 2.playbook level    ----2nd highest priority
 3.inventory level -- low priorty
   a.host level variabel
   b. group level

Inventory variables: These are defined in the inventory file (or dynamic inventory) for specific hosts or groups.

[webservers]
ansiblenode1@172.31.20.135  package_name=git
ansiblenode2@172.31.30.200 package_name=apache2
localhost 

[webservers:vars]
ansiblenode2@172.31.30.200 
localhost 

package_name=httpd

Playbook variables: You can define variables directly within your playbooks using the vars section.

---
- hosts: Webservers

  become: yes

  vars:

  pacakge_name: git

  tasks:
    
    - name: Install all packages

      apt:

      name: "{{ pacakge_name }}"

      state: present

      Command-line variables: You can pass variables to your playbooks at runtime using the -e or --extra-vars option.
      

      >ansible-playbook -i hosts -e "package_name=apache2" variables2.yml



Ansible resolves variable values based on a specific precedence order. The order from highest to lowest precedence is:
====================================================================================================================

Extra-vars (-e on the command line): Command-line variables take the highest precedence.

Playbook variables: Variables defined within the playbook.

Inventory variables: Variables set in the inventory.

Working Script::
===================


---
- hosts: Websevers
- 
  become: yes
  
  vars:
  
    package_name: apache2
  
    package_httpd: httpd
  
    git_variable: git
  
  tasks:
  
  -  name: installed apache
  -  
     apt:
       name: "{{ package_name }}"
     
       state: present
     
       update_cache: yes
     
     when: ansible_os_family=="Debian"
     
  -  name: installed git
  
     apt:
       name: "{{ git_variable }}"
     
       state: present
     
     when: ansible_os_family=="Debian"
     
  -  name: installed httpd
     yum:
       name: "{{ package_httpd }}"
     
       state: present
     
     when: ansible_os_family=="Redhat"



20/06/2025::
================


Debug & vars & register in Ansible module::
==========================================

https://docs.ansible.com/ansible/latest/collections/ansible/builtin/debug_module.html

---
- name: Echo message on localhost

  hosts: localhost

   connection: local

   gather_facts: no

   vars:

   message: "Hello from Ansible playbook on localhost!"

  tasks:
    
    - name: Echo message and connection type

      ansible.builtin.shell: "echo '{{ message }}' ; echo 'Connection type: {{ ansible_connection }}'"

      register: echo_output

    
    - name: Display output

      debug:

      msg: "{{ echo_output.stdout_lines }}"


>ansible-playbook -i hosts -vvv variable.yaml  --------> verbose logs purpose ,please run this command


![image](https://github.com/user-attachments/assets/7d18a6e5-a53b-436b-bf26-dbe1db0e89af)


Registry Module::
-----------------
Registry is a module used to results can be stored in a variable
Stored ouptput of a task or script
I want execute a command and results can be stored in a variable is called registry

Handlers::
===========
Sometimes you want a task to run only when a change is made on a machine. For example, you may want to restart a service if a task updates the configuration of that service, but not if the configuration is unchanged. Ansible uses handlers to address this use case. Handlers are tasks that only run when notified

---
  hosts: webservers
  become: yes
  tasks:
    - name: Ensure apache is at the latest version
      ansible.builtin.yum:
        name: httpd
        state: latest
  handlers:
    - name: Restart apache
      ansible.builtin.service:
        name: httpd
        state: restarted


Working Playbook, please try to execute and understand::
========================================================


- hosts: DBservers
  become: yes
  tasks:
  - name: install apache2
    apt:
      name: apache2
      state: present
      update_cache: yes
  - debug:
      msg: "install apache2 successfully in ubuntu machines"
  - name: install my sql software
    apt:
      name: mysql-server
      state: present
  - debug:
      msg: "install mysql-server successfully in ubuntu machines"

  - name: install php
    apt:
      name: php
      state: present
  - debug:
      msg: "install php successfully in ubuntu machines"

  - name: install libapache2-mod-php
    apt:
      name: libapache2-mod-php
      state: present
  - debug:
      msg: "install mod php successfully in ubuntu machines"

  - name: install php-mcrypt
    apt:
      name: php-mcrypt
      state: present
  - debug:
      msg: "install mcrypt successfully in ubuntu machines"

  - name: install php-mysql
    apt:
      name: php-mysql
      state: present
  - debug:
      msg: "install mysql successfully in ubuntu machines"
  handlers:
  - name: restart apache2
    service:
      name: apache2
      enabled : yes
      state: stopped
  handlers:
  - name: start apache2
    service:
      name: apache2
      enabled : yes
      state: started

  - name: install php-cli
    apt:
      name: php-cli
      state: present
  - debug:
      msg: "install php-cli successfully in ubuntu machines"

  - name: restart apache2
    service:
      name: apache2
      enabled : yes
      state: restarted

  - name: Copy file with src and destination
    copy:
      src: info.php
      dest: /var/www/html/info.php



=========================

Working Script::


---
- hosts: Websevers
  become: yes
  tasks:     
  -  name: install all php packages in ubuntu machines
     apt:
       name: "{{ item }}"
       state: present     
     loop:
       - php-fpm
       - php-mysql
       - php-opcache
       - php-cli
       - libapache2-mod-php
  -  debug:
       msg: "installed all the PHP packages"      
  handlers:
  -  name: install Apache2 in ubuntu machines
     apt:
       name: apache2
       state: present
  -  debug:
       msg: "installed apache2 successfully"     
  -  name: apache2 started in ubuntu machines
     service:
       name: apache2
       enabled: yes
       state: started 
  -  debug:
       msg: "aapche2 started successfully"          
  -  name: apache2 enabled in ubuntu machines
     service:
       name: apache2
       enabled: yes
       state: reloaded
  -  debug:
       msg: "apache2 reloaded successfully"      
  -  name: apache2 restarted in ubuntu machines
     service:
       name: apache2
       enabled: yes
       state: restarted
  -  debug:
       msg: "apache2 restaretd successfully"      
  -  name: Copy info.php file to Destination folder
     copy:
       src: info.php
       dest: /var/www/html/info.php
  -  debug:
       msg: "copied php file successfully"




23/06/2025:: And 24/06/2025::
============================

Ansible Roles::
===================


![image](https://github.com/user-attachments/assets/99525357-1651-471a-b737-df79823dc24f)


Ansible roles are a way of organizing playbooks and tasks in a modular, reusable, and maintainable structure. They allow you to break down complex playbooks into smaller, focused units of functionality that can be easily shared and reused across different projects. Here's a more detailed look at Ansible roles:

https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_reuse_roles.html

1.Written ansible in a reusable fashion
2.How do I use someone else’s work
3.Ansible galaxy is a place where we can find reusable roles

https://galaxy.ansible.com/

4.Which we can use in your script



install roles

 > Ansible-galaxy install <rolename>

 >ansible-galaxy install my_role

create my own role::

> ansible-galaxy init <rolename>

>ansible-galaxy init my_role



Structure of Ansible Roles::
===================

my_role/
├── defaults/
│   └── main.yml            # Default variables
├── files/
│   └── somefile            # Files to be copied to the target
├── handlers/
│   └── main.yml            # Handlers (usually for service restarts)
├── meta/
│   └── main.yml            # Metadata about the role
├── tasks/
│   └── main.yml            # The main tasks (this file includes other task files if needed)
├── templates/
│   └── config.j2           # Jinja2 templates for dynamic file creation
├── tests/
│   └── test.yml            # Test playbooks to verify the role works
├── vars/
│   └── main.yml            # Custom variables


Using Roles in Playbooks
Once you've defined a role, you can use it in your playbook like this:

---
- name: Example Playbook using roles
  hosts: all
  become: yes
  roles:
    - my_role

Benefits of Using Roles
Reusability: Roles can be reused across different playbooks and projects.

Modularity: Roles allow you to organize your playbook into smaller, manageable parts.

Clarity: Each role focuses on a specific task or function, making your playbooks more understandable.

Example Role: Installing Tomcat

https://galaxy.ansible.com/ui/standalone/roles/robertdebock/tomcat/install/


Create my own role

> Ansible-galaxy init rolename

![image](https://github.com/user-attachments/assets/af275783-63b6-40ab-a319-645db283a40f)

![image](https://github.com/user-attachments/assets/34cfe34b-b8bc-4026-9014-0c07c952c3af)

Install tomcat

If you're looking to install or use an Ansible role for Tomcat from Ansible Galaxy, you can search for available roles and collections related to Tomcat. Here's how you can find and use a role related to Tomcat from Galaxy.
1.	Search for a Tomcat Role

https://galaxy.ansible.com/

To search for a role related to Tomcat on Ansible Galaxy, you can use the following command:
bash
Copy
ansible-galaxy search tomcat
This will return a list of roles related to Tomcat that you can install and use.
2. Install a Tomcat Role
Once you’ve found a suitable role for Tomcat, you can install it using the ansible-galaxy install command.
For example, if you find a role called geerlingguy.tomcat, you can install it by running:
bash
Copy
> ansible-galaxy install geerlingguy.tomcat
This will download and install the role into your ~/.ansible/roles/ directory (or the path defined in your ansible.cfg file).
3. Use the Installed Tomcat Role in Your Playbook
After installing the role, you can use it in your playbook. Here’s an example of a simple playbook that installs and configures Tomcat:
yaml
Copy

Deploywar.yml::
=============

---
- hosts: localhost
  become: yes
  roles:
  - robertdebock.java
  - robertdebock.tomcat
 
  > ansible-playbook -i hosts Deploywar.yml
  

![image](https://github.com/user-attachments/assets/306fd1fc-8c51-40f7-81b6-41a44e6ee915)

  
This will use the geerlingguy.tomcat role to set up Tomcat on your webservers hosts.

https://galaxy.ansible.com/robertdebock/tomcat

![image](https://github.com/user-attachments/assets/29cfc5e4-b8e6-494b-a462-d8a11699df12)

Deploywar.yml

![image](https://github.com/user-attachments/assets/d7f4d510-bee2-4d32-ad56-7906a8574e93)

![image](https://github.com/user-attachments/assets/adad9ea6-ed52-457e-a9eb-adb2d19ad026)

![image](https://github.com/user-attachments/assets/a4c880aa-f378-4085-9122-3ef93a25e09a)


By default  tomcat run port 8080
http://18.236.181.244:8080/
http://34.216.173.44:8080/manager/html

![image](https://github.com/user-attachments/assets/fa5faaeb-ec9e-43f2-9184-7bf46f1433c4)


Most of the work is done 
Where is my war file


Deploy Onlinebook store war to tomcat server using roles::
==============================================================

>If war file is available in local machine use copy module
>if war file is available other machine(internet) use get_url module
Tomcat by default install

>/opt/tomcat

![image](https://github.com/user-attachments/assets/45a19e09-7641-4dec-b730-d2b01a3ea63b)

![image](https://github.com/user-attachments/assets/721d2e75-0368-4d87-bdf1-d54331ef8afb)

---
- hosts: Webservers
  become: yes
  roles:
  - robertdebock.java
  - robertdebock.tomcat
  tasks:
  - name: copy war
    get_url:
      url: https://srinfotech.s3.us-west-2.amazonaws.com/jobs/AnsibleIntegartedWith+Jenkins/5/onlinebookstore.war
      dest: /opt/tomcat/webapps/onlinebookstore.war


![image](https://github.com/user-attachments/assets/d43d4d4a-ee8d-4dd8-af09-b71dfdf2da6f)

Create S3 Bucket in AWS account::
===============================

Go to AWS account and search S3 bucket 

S3=SSS=simple storage services

![image](https://github.com/user-attachments/assets/8c1b5637-9392-414d-ab0b-21bf9d882609)

Select S3

![image](https://github.com/user-attachments/assets/c62a298f-185d-43ec-9d62-8b874e7627ec)

Click Create bucket

![image](https://github.com/user-attachments/assets/097eedf8-8e2f-48f5-876f-2c3debfccda8)

Bucket name provide

![image](https://github.com/user-attachments/assets/669f5b5a-d4e4-43ee-add1-e6be36171ec4)

Object Ownership  ---- ACLs enabled selected


Unchecked Block all public access


![image](https://github.com/user-attachments/assets/61cac919-cbbd-4b39-9121-d1ed20e33bcd)

Ackened 

![image](https://github.com/user-attachments/assets/9edcd3b0-c71a-4e78-8132-0469a192cd82)

Click crete bucket

![image](https://github.com/user-attachments/assets/c0b39afe-325c-4d82-9ea6-2204896c1f55)

S3 bucket is created in AWS

![image](https://github.com/user-attachments/assets/702e2185-29cd-43d2-9176-ad9788907bc8)

S3 bucket Created successfully


![image](https://github.com/user-attachments/assets/3c2855d7-ae2c-4f18-8ce7-3b766211b811)

Click Bucket

![image](https://github.com/user-attachments/assets/3000b5bc-8691-40cc-b5ee-e378fe813bf6)


Click Upload 


![image](https://github.com/user-attachments/assets/71efca18-9c4a-4bad-97ff-6e6baf6b559c)

Click Add Files


![image](https://github.com/user-attachments/assets/e74175f3-ca04-47bb-977b-9f9df1cf7139)

Select Onlinebookstore.war file

![image](https://github.com/user-attachments/assets/89cac099-5c85-4a29-91e9-8868f2e2f020)

Select check box to upload the onlinebookstore.war file

![image](https://github.com/user-attachments/assets/30c81ce3-4605-45e9-90bd-b719dac4d875)

Click Upload

![image](https://github.com/user-attachments/assets/85a5204d-b660-4d0c-8983-fc24b05427e4)

Upload Succeeded

![image](https://github.com/user-attachments/assets/11d79c2d-c353-404c-be41-130608b34dcb)

Copy URL

![image](https://github.com/user-attachments/assets/147864ff-fc89-4ae1-b104-b383cccba33b)

![image](https://github.com/user-attachments/assets/37ad0996-d054-4a3b-aa57-c0480254c1c1)

Copy url to below script:: onlinebookstore.yml
===================

---
- hosts: localhost
  become: yes
  roles:
  - robertdebock.java
  - robertdebock.tomcat
  tasks:
  - name: copy war
    get_url:
      url: https://srinfotech.s3.us-west-2.amazonaws.com/jobs/AnsibleIntegartedWith+Jenkins/5/onlinebookstore.war
      dest: /opt/tomcat/webapps/onlinebookstore.war

![image](https://github.com/user-attachments/assets/402272bc-6604-4840-a406-c1cc8e95dcc6)

run the playbook

>ansible-playbook -i hosts onlinebookstore.yml

![image](https://github.com/user-attachments/assets/4ed55d65-f16e-4314-8dba-c3a34c3ee5c2)

Success

![image](https://github.com/user-attachments/assets/592b947e-d422-4430-9729-98724403ce0d)

Verify deployment in Tomcat server

![image](https://github.com/user-attachments/assets/c50103d8-21ba-484e-8562-34a1b5b2c0d0)

http://54.218.133.244:8080/onlinebookstore/

![image](https://github.com/user-attachments/assets/e79ac48a-f76e-42ff-b5a5-28094402c20a)


Integrated Ansible & Tomcat & S3 With Jenkins::
===============================================





S3 bucket creation and integrate S3 with Jenkins::
=====================================================

Go to AWS account and search S3 bucket 

S3=SSS=simple storage services


![image](https://github.com/user-attachments/assets/24bc6c86-9063-4d41-9f91-165cdb6238dc)

 

Select S3

![image](https://github.com/user-attachments/assets/91b082dc-65f2-46be-8800-997cd38e117b)

 

Click Create bucket

 ![image](https://github.com/user-attachments/assets/147baac9-7372-4b3e-9586-77687b9722c6)


AWS region  --virgenia

![image](https://github.com/user-attachments/assets/fd820852-8d1b-49eb-b8a4-9b33c18e70b7)


Bucket name provide


 

Object Ownership  ---- ACLs enabled selected


 ![image](https://github.com/user-attachments/assets/d1928ba2-8b6e-4df9-b68d-d94cc15326b8)


Unchecked Block all public access


 ![image](https://github.com/user-attachments/assets/813ea825-a67f-4b77-af97-338992d19d6e)


Ackened 

 ![image](https://github.com/user-attachments/assets/7b2a5776-e82e-4e4a-921f-1fb75aa02edc)


Click crete bucket



![image](https://github.com/user-attachments/assets/acfc10ae-76e4-4bb0-bb3e-caaa4c4f429d)

 

S3 bucket is created in AWS


![image](https://github.com/user-attachments/assets/23c158bb-207d-4a00-8b20-eed9881438e9)

 

First installed Jenkins in AWS ubuntu machine

Installed S3 publisher plugin

Found S3 profile at system configuration


![image](https://github.com/user-attachments/assets/cff577be-a2db-4ee0-b5f3-bfda98ae7384)

 

Second step::
Create IAM role in AWS account

 IAM----> Indentity Access Management

![image](https://github.com/user-attachments/assets/4cbba43f-c06d-43b6-8a27-3dc5c76e4ec2)


![image](https://github.com/user-attachments/assets/56b9485f-2538-4558-9963-a0253328a2f8)

 

Click Users

![image](https://github.com/user-attachments/assets/5178b83a-f01a-43c5-901b-82aa693ff52d)

 

Click create user


 ![image](https://github.com/user-attachments/assets/f9c443d3-4172-475c-92fd-d55f8bac2363)


Provide the user name


![image](https://github.com/user-attachments/assets/03fa6ef0-f565-47eb-a288-e9db884cb3dd)

 
![image](https://github.com/user-attachments/assets/63632b00-66bf-494e-8d25-dfd4b7a8fe46)

 
Click next
 
![image](https://github.com/user-attachments/assets/5ccb8d94-9dd7-4823-b336-64e1f40185e0)

![image](https://github.com/user-attachments/assets/0ebcab66-285f-4498-97b9-eac4c1f1d116)
 

![image](https://github.com/user-attachments/assets/61351716-26ce-4f59-abcc-95423a19bb83)

 
 
select S3 policies


 ![image](https://github.com/user-attachments/assets/4108108b-fd6b-4b41-98af-f75c846ade4d)



User created successfully


![image](https://github.com/user-attachments/assets/9c932e66-b49a-4c79-9acd-e475ce79e89e)

 
User name::

SRInfotech

Console password::

wv9PC8%3


![image](https://github.com/user-attachments/assets/7e60afc9-f167-458d-bbd1-dbee13f0668a)

  


Create access & secret keys:;

Open new user test


 ![image](https://github.com/user-attachments/assets/0c2db911-ee73-49fa-8521-65b54ec681b9)


Click create access key

 ![image](https://github.com/user-attachments/assets/6a165b7e-fbcd-4c02-bae8-7b0d725a45c1)



Select Application running on an AWS compute service


![image](https://github.com/user-attachments/assets/ef231f9a-1511-430f-a4f9-d5555e903d84)

 

Click next


 ![image](https://github.com/user-attachments/assets/b17aa07c-f4e6-4657-a0c8-a8144a2bee0c)


Access keys created


![image](https://github.com/user-attachments/assets/4a5d2768-8666-4c15-96b1-fe050ee523f3)

 
 ![image](https://github.com/user-attachments/assets/07429f2c-a808-4fc6-9908-296c3513ed42)



Integaretd S3 with Jenkins


![image](https://github.com/user-attachments/assets/e665dc0a-43b6-41dd-8ce7-90bc7cdd1e0a)

 

Provided access and secret key

Click test connection


![image](https://github.com/user-attachments/assets/9290abf9-a675-4a0a-ab68-9c46678b83e2)

 

Check passed


 ![image](https://github.com/user-attachments/assets/56db73d5-9d8d-4f6b-9df9-4c76e746de5f)


Bucket region us-east-1

 

 ![image](https://github.com/user-attachments/assets/5179600c-c962-4000-92c9-f78e34ccd596)

 

 

Destination bucket:: should be give AWS bucket name

 
![image](https://github.com/user-attachments/assets/8273aff6-f175-41fa-a0c2-7c0ba697f74d)

 
![image](https://github.com/user-attachments/assets/9d35ced8-7e52-4ef3-973d-9fbfdb354f24)


 ![image](https://github.com/user-attachments/assets/6f78f94c-c349-4c21-ab45-bb14f5c44400)

![image](https://github.com/user-attachments/assets/04ef0eef-31ff-4cb4-a152-74b97dbc3b37)


![image](https://github.com/user-attachments/assets/560d116a-206a-4688-9711-620198f6cfad)


![image](https://github.com/user-attachments/assets/2d1d7dd4-f351-4752-928f-28377c2d9ad8)


![image](https://github.com/user-attachments/assets/6819247b-1cf8-4265-b04b-e79adf3d4051)

![image](https://github.com/user-attachments/assets/db23a9d6-5725-41d8-9083-55173325b240)


 ![image](https://github.com/user-attachments/assets/77a787c6-07bb-4c22-93fc-07939f1eb36c)

![image](https://github.com/user-attachments/assets/2cfade4f-e8c7-4254-bbcf-e103d84c13c2)



![image](https://github.com/user-attachments/assets/5eaccb62-252d-4a3e-9d53-4768cf153b69)
Should be enabled Manage artifacts options
 

 

  26/06/2025::
  ================

Docker Introductions::
=================

Docker is an opensource & Applicatuions level virtualization technology and it's called containirazition.

Docker is an open-source platform that automates the deployment, scaling, and management of applications in lightweight, portable containers. Containers are isolated environments that package an application and all its dependencies (such as libraries, binaries, and configurations) to ensure it runs uniformly across different computing environments.

![image](https://github.com/user-attachments/assets/c3b1350c-eb6b-44f1-94b1-0c05b65c3653)

Docker is a platform and that make it easier to create, deploy, and run applications using containers. Containers are lightweight, standalone, and executable units that include everything needed to run a piece of software, including the code, runtime, libraries, and system tools.

container ::
==============
1.container is an insolation area of executuions of your applications
 OR
 instance of images are called containers
2.Containers are created from “images”
3. Containers are the core of Docker. They are lightweight, portable, and isolated environments where applications run.
  Docker is run your software packages /Applications  in containers called containarizations.

4. if you build a docker container for your application called containerization
5. containers have it’s own boundaries  

who will create containers?
Ans --docker images are created the containers

 Docker Images:
 ===============

 docker image is a package with all dependencies and the necessary 
information to create the container and docker image derived from multiple base images.

An image is a snapshot of a container, a blueprint that defines what the container will contain and how it will behave when run. It consists of an application and its dependencies. Docker images are built using a Dockerfile

Docker Registry::
====================

A Docker Registry is a system for storing and distributing Docker images. It is a centralized location where Docker images can be uploaded (pushed), stored, and downloaded (pulled) by users and applications. Docker images are the building blocks of containers, and registries provide a way to manage, version, and share these images across different environments.

Default registry :: https://hub.docker.com/

Physical & Virtual & Hypervisors/VMwares::
=============================================

1.tomcat & nodejs containers have it’s own process tree,own files systems,own network interfaces own storage,ram…etc
2.when you want to give application to your team/testers  docker is the best choice and when you want give system to your team/ testers VMwares are best choice.
3.application level virtulization docker is the best choice and OS level virtulization VMwares are best choice
4.individually scale the your application very easy in docker

![image](https://github.com/user-attachments/assets/c3b1350c-eb6b-44f1-94b1-0c05b65c3653)


Example:: For festival season In your organization leave management application multiple employees are applied leaves at the same time in that scenario docker is very easy to scale the one more application but physically it’s very difficult so docker is the best choice


![image](https://github.com/user-attachments/assets/c3b1350c-eb6b-44f1-94b1-0c05b65c3653)





27/06/2025::
=============

Install Docker in Ubuntu machine::
=====================================

Please follow below link steps to install the docker in ubuntu and please read all the content in that link

https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-22-04

once installed docker please verify below commands::

>docker --version

root@ip-172-31-20-86:~# docker --version
Docker version 28.0.4, build b8034c0

root@ip-172-31-20-86:~# docker info
Client: Docker Engine - Community
 Version:    28.0.4
 Context:    default
 Debug Mode: false
 Plugins:
  buildx: Docker Buildx (Docker Inc.)
    Version:  v0.22.0
    Path:     /usr/libexec/docker/cli-plugins/docker-buildx
  compose: Docker Compose (Docker Inc.)
    Version:  v2.34.0
    Path:     /usr/libexec/docker/cli-plugins/docker-compose

Server:
 Containers: 0
  Running: 0
  Paused: 0
  Stopped: 0
 Images: 0
 Server Version: 28.0.4
 Storage Driver: overlay2
  Backing Filesystem: extfs
  Supports d_type: true
  Using metacopy: false
  Native Overlay Diff: true
  userxattr: false
 Logging Driver: json-file
 Cgroup Driver: systemd
 Cgroup Version: 2
 Plugins:
  Volume: local
  Network: bridge host ipvlan macvlan null overlay
  Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog
 Swarm: inactive
 Runtimes: io.containerd.runc.v2 runc
 Default Runtime: runc
 Init Binary: docker-init
 containerd version: 05044ec0a9a75232cad458027ca83437aae3f4da
 runc version: v1.2.5-0-g59923ef
 init version: de40ad0
 Security Options:
  apparmor
  seccomp
   Profile: builtin
  cgroupns
 Kernel Version: 6.8.0-1024-aws
 Operating System: Ubuntu 24.04.2 LTS
 OSType: linux
 Architecture: x86_64
 CPUs: 2
 Total Memory: 3.82GiB
 Name: ip-172-31-20-86
 ID: 201c6f4b-75d3-4326-adf5-00b9a82a8d4d
 Docker Root Dir: /var/lib/docker
 Debug Mode: false
 Experimental: false
 Insecure Registries:
  ::1/128
  127.0.0.0/8
 Live Restore Enabled: false

if above page is came without any erros, it means docker is installed in your machine


Docker High Level Client -Server Architecture::
==================================


![image](https://github.com/user-attachments/assets/78e4ca62-008e-425a-909a-bab59e3030ed)


Docker's high-level architecture revolves around several components that work together to provide containerization and isolation for applications


Docker Client (CLI)::
=================

The Docker Client is the primary interface for interacting with Docker. It can be a command-line interface (CLI), like the docker command, or a graphical interface (GUI) in some tools.

It allows users to interact with Docker's features, such as building containers, running containers, and managing containers and images.

It sends requests to the Docker Daemon to execute commands.

Docker Daemon (Dockerd)::
====================

The Docker Daemon (also known as dockerd) is the core component of Docker. It runs in the background on the host system.

The daemon is responsible for managing Docker containers, images, networks, and volumes. It listens for Docker API requests and handles container lifecycle operations such as starting, stopping, and building containers.

The Docker Daemon can communicate with multiple Docker clients, allowing for distributed management of containers.

Flow:
============
1.The Docker Client sends a command to the Docker Daemon.

2.The Docker Daemon interacts with containers, images, and storage volumes.

3.The Docker Daemon can pull images from a Docker Registry.

4.The Docker Daemon runs containers based on the images and handles networking and storage.

Docker commands::
====================

 >docker pull <imagename>

 >docker pull hello-world

 >docker images   ----used to display the all images

 > docker image ls ----used to display the all images
 
 >docker run ---used to build the images and create the container

Create the Jenkins container::
=================================

>docker run -d -p 8080:8080 -p 5000:5000 jenkins/jenkins:jdk21


http://35.155.150.89:8080/


![image](https://github.com/user-attachments/assets/30576b75-b3ee-47e1-97f0-f535c46ff015)


>docker ps

above command is used to verify the how many containers are running


Create the Nginx web based application container::
=======================================================

>docker run -d -p 80:80 nginx:latest

http://35.155.150.89/

![image](https://github.com/user-attachments/assets/003a7ca7-5a81-4ea6-8b60-3c1dd0b7a74d)


>docker ps

above command is used to verify the how many containers are running, you can seee nginx container is running state



detached mode::
=================

Docker detached mode refers to running a container in the background

>docker run -d <image_name>

example::
> docker run -d nginx

Where:

-d is the flag for detached mode.

<image_name> is the name of the Docker image you want to run.

> docker run -d nginx

This command will:

Run the nginx container in detached mode.

Start the container in the background.

To view the containers running in detached mode, you can use the docker ps command:
======================================

>docker ps

Stopping a Container::
=================

>docker stop <containerID>

Start a Container::
=================

>docker start <containerID>

To run a command inside a running container:
======================

>docker exec -it <container_id_or_name> <command>
>docker exec -it 5336d949f33b /bin/bash

>root@5336d949f33b:/# hostname
5336d949f33b
>root@5336d949f33b:/# hostname -i
172.17.0.3


![image](https://github.com/user-attachments/assets/c7114894-3fcd-46b0-b393-6f296d23b845)

NOTE:::
=========

>docker exec -it 5178eb58223a /bin/bash
Use this command inside the container

>ctrl pq
Outside the containers

Lab practice::
===============

take one nginx web server

>docker pull nginx

root@ip-172-31-20-86:~# docker pull nginx
Using default tag: latest
latest: Pulling from library/nginx
6e909acdb790: Pull complete
5eaa34f5b9c2: Pull complete
417c4bccf534: Pull complete
e7e0ca015e55: Pull complete
373fe654e984: Pull complete
97f5c0f51d43: Pull complete
c22eb46e871a: Pull complete
Digest: sha256:124b44bfc9ccd1f3cedf4b592d4d1e8bddb78b51ec2ed5056c52d3692baebc19
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest

>docker images

root@ip-172-31-20-86:~# docker images
REPOSITORY        TAG       IMAGE ID       CREATED        SIZE
jenkins/jenkins   latest    be95e0848c42   7 days ago     466MB
nginx             latest    53a18edff809   7 weeks ago    192MB

>docker run -d -p 80:80 nginx

root@ip-172-31-20-86:~# docker run -d -p 80:80 nginx
3d1a52d091b05878e079b89002aa57b460c5263a585a8add0ecc671608d1f999

>docker ps

root@ip-172-31-20-86:~# docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS                                 NAMES
3d1a52d091b0   nginx     "/docker-entrypoint.…"   3 seconds ago   Up 3 seconds   0.0.0.0:80->80/tcp, [::]:80->80/tcp   thirsty_shaw

>docker exec -it 3d1a52d091b0

root@ip-172-31-20-86:~# docker exec -it 3d1a52d091b0  /bin/bash
docker: 'docker exec' requires at least 2 arguments

root@ip-172-31-20-86:~# docker exec -it 3d1a52d091b0 /bin/bash
root@3d1a52d091b0:/# hostname
3d1a52d091b0
root@3d1a52d091b0:/# hostname -i
172.17.0.3

root@5336d949f33b:/# ls
bin  boot  dev  docker-entrypoint.d  docker-entrypoint.sh  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@5336d949f33b:/# cd opt/
root@5336d949f33b:/opt# ls
root@5336d949f33b:/opt# cd ..
root@5336d949f33b:/# ls
bin  boot  dev  docker-entrypoint.d  docker-entrypoint.sh  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
root@5336d949f33b:/# cd usr/
root@5336d949f33b:/usr# ls
bin  games  include  lib  lib64  libexec  local  sbin  share  src
root@5336d949f33b:/usr# cd lib
root@5336d949f33b:/usr/lib# ls
apt  dpkg  init  locale  lsb  mime  nginx  os-release  sasl2  ssl  systemd  terminfo  tmpfiles.d  udev  x86_64-linux-gnu
root@5336d949f33b:/usr/lib#
root@5336d949f33b:/usr/lib# docker images
bash: docker: command not found
root@5336d949f33b:/usr/lib# docker imagesexit
bash: docker: command not found
root@5336d949f33b:/usr/lib# read escape sequence
root@ip-172-31-20-86:~# docker images
REPOSITORY        TAG       IMAGE ID       CREATED        SIZE
jenkins/jenkins   latest    be95e0848c42   7 days ago     466MB
nginx             latest    53a18edff809   7 weeks ago    192MB
ubuntu            latest    a04dc4851cbc   2 months ago   78.1MB
hello-world       latest    74cc54e27dc4   2 months ago   10.1kB
root@ip-172-31-20-86:~# docekr runRead from remote host ec2-34-204-17-141.compute-1.amazonaws.com: Connection reset by peer
Connection to ec2-34-204-17-141.compute-1.amazonaws.com closed.
client_loop: send disconnect: Connection reset by peer

we can see below nginx web page and nginx is running on containers

![image](https://github.com/user-attachments/assets/878995bc-58b1-4f20-982e-2d60f105891d)



Lab Practice::
====================


root@ip-172-31-39-182:~# docker images
REPOSITORY        TAG       IMAGE ID       CREATED        SIZE
jenkins/jenkins   jdk21     52e1941f479f   21 hours ago   471MB
root@ip-172-31-39-182:~# docker run -d -p 8080:8080 -p 5000:5000 jenkins/jenkins:jdk21
aca7ec14bfc5f057f73dc4cf294e920a63712bbd5f838b5205e5e00faa542318
root@ip-172-31-39-182:~# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED         STATUS         PORTS                                                                                                 NAMES
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   7 seconds ago   Up 6 seconds   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp   festive_tharp
root@ip-172-31-39-182:~# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                 NAMES
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   43 seconds ago   Up 43 seconds   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp   festive_tharp
root@ip-172-31-39-182:~# java --version
Command 'java' not found, but can be installed with:
apt install default-jre              # version 2:1.17-75, or
apt install openjdk-17-jre-headless  # version 17.0.14+7-1~24.04
apt install openjdk-21-jre-headless  # version 21.0.6+7-1~24.04.1
apt install openjdk-19-jre-headless  # version 19.0.2+7-4
apt install openjdk-20-jre-headless  # version 20.0.2+9-1
apt install openjdk-22-jre-headless  # version 22~22ea-1
apt install openjdk-11-jre-headless  # version 11.0.26+4-1ubuntu1~24.04
apt install openjdk-8-jre-headless   # version 8u442-b06~us1-0ubuntu1~24.04
root@ip-172-31-39-182:~# docker exec -it aca7ec14bfc5 /bin/bash
jenkins@aca7ec14bfc5:/$ java --version
openjdk 21.0.7 2025-04-15 LTS
OpenJDK Runtime Environment Temurin-21.0.7+6 (build 21.0.7+6-LTS)
OpenJDK 64-Bit Server VM Temurin-21.0.7+6 (build 21.0.7+6-LTS, mixed mode)
jenkins@aca7ec14bfc5:/$ sudo apt update
bash: sudo: command not found
jenkins@aca7ec14bfc5:/$ hostname
aca7ec14bfc5
jenkins@aca7ec14bfc5:/$ java --version
openjdk 21.0.7 2025-04-15 LTS
OpenJDK Runtime Environment Temurin-21.0.7+6 (build 21.0.7+6-LTS)
OpenJDK 64-Bit Server VM Temurin-21.0.7+6 (build 21.0.7+6-LTS, mixed mode)
jenkins@aca7ec14bfc5:/$ cd /var/lib/
jenkins@aca7ec14bfc5:/var/lib$ ls
apt  dpkg  git  misc  pam  shells.state  systemd
jenkins@aca7ec14bfc5:/var/lib$ exit
exit
root@ip-172-31-39-182:~# cd /var/lib/
root@ip-172-31-39-182:/var/lib# ls
PackageKit  command-not-found  grub           os-prober     shim-signed              ucf
amazon      containerd         hibinit-agent  pam           snapd                    udisks2
app-info    dbus               ieee-data      plymouth      sudo                     unattended-upgrades
apport      dhcpcd             landscape      polkit-1      swcatalog                update-manager
apt         docker             libuuid        private       systemd                  update-notifier
boltd       dpkg               logrotate      python        tpm                      usb_modeswitch
chrony      fwupd              man-db         sgml-base     ubuntu-advantage         vim
cloud       git                misc           shells.state  ubuntu-release-upgrader  xml-core
root@ip-172-31-39-182:/var/lib# cd ..
root@ip-172-31-39-182:/var# cd ..
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED         STATUS         PORTS                                                                                                 NAMES
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   7 minutes ago   Up 7 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp   festive_tharp
root@ip-172-31-39-182:/# docker exec -it aca7ec14bfc5 /bin/bash
jenkins@aca7ec14bfc5:/$ cd /var/jenkins_home/secret
bash: cd: /var/jenkins_home/secret: No such file or directory
jenkins@aca7ec14bfc5:/$ ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
jenkins@aca7ec14bfc5:/$ cd secrets
bash: cd: secrets: No such file or directory
jenkins@aca7ec14bfc5:/$ cd ..
jenkins@aca7ec14bfc5:/$ ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
jenkins@aca7ec14bfc5:/$ pwd
/
jenkins@aca7ec14bfc5:/$ cd /var/jenkins_home/
jenkins@aca7ec14bfc5:~$ ls
config.xml                     jenkins.telemetry.Correlator.xml  plugins                   secrets      users
copy_reference_file.log        jobs                              secret.key                updates      war
hudson.model.UpdateCenter.xml  nodeMonitors.xml                  secret.key.not-so-secret  userContent
jenkins@aca7ec14bfc5:~$ cd secrets
jenkins@aca7ec14bfc5:~/secrets$ ls
initialAdminPassword  jenkins.model.Jenkins.crumbSalt  master.key
jenkins@aca7ec14bfc5:~/secrets$ cat initialAdminPassword
3268b754fc93442e9ea3cf22c40fcc8e
jenkins@aca7ec14bfc5:~/secrets$ read escape sequence
root@ip-172-31-39-182:/# docker run -d -p 8080:8080 -p 5000:5000 jenkins/jenkins:jdk21
1b6159a409c358d5a2db6ecc34b13cf29e8f1d94ca249722a47424d02a8d6bc1
docker: Error response from daemon: failed to set up container networking: driver failed programming external connectivity on endpoint unruffled_pare (f76e7f84de1872354f3caf9f2c4d2ee9bf83c468178a614d407f1c5d35df00f3): Bind for 0.0.0.0:5000 failed: port is already allocated

Run 'docker run --help' for more information
root@ip-172-31-39-182:/# docker run -d -p 8081:8081 -p 5001:5001 jenkins/jenkins:jdk21
601ef30a9a97b2ef1ab13a6956d603edbc23cd2d2717cb4d2db41f4b88e148ae
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   8 seconds ago    Up 8 seconds    0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   12 minutes ago   Up 12 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS              PORTS                                                                                                           NAMES
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   2 minutes ago    Up About a minute   0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   14 minutes ago   Up 14 minutes       0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   3 minutes ago    Up 3 minutes    0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   16 minutes ago   Up 16 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker exec -it 601ef30a9a97 /bin/bash
jenkins@601ef30a9a97:/$ java --version
openjdk 21.0.7 2025-04-15 LTS
OpenJDK Runtime Environment Temurin-21.0.7+6 (build 21.0.7+6-LTS)
OpenJDK 64-Bit Server VM Temurin-21.0.7+6 (build 21.0.7+6-LTS, mixed mode)
jenkins@601ef30a9a97:/$ cd /var/jenkins_home/
jenkins@601ef30a9a97:~$ ls
config.xml                     jenkins.telemetry.Correlator.xml  plugins                   secrets      users
copy_reference_file.log        jobs                              secret.key                updates      war
hudson.model.UpdateCenter.xml  nodeMonitors.xml                  secret.key.not-so-secret  userContent
jenkins@601ef30a9a97:~$
jenkins@601ef30a9a97:~$ exit
exit
root@ip-172-31-39-182:/# docker run -d -p 8585:8585 jenkins/jenkins:jdk21
bc684af40e16b2c7eb91de87e952ec7a1ae0bab608bc9d0e17bad723ce853d69
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
bc684af40e16   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   7 seconds ago    Up 7 seconds    8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   7 minutes ago    Up 7 minutes    0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   19 minutes ago   Up 19 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker run -d -p 80:80 jenkins/jenkins:jdk21
a800fb0e6d7cd81cefdb33b1ded7019c478fbd8ebd232498c99316a092b92660
root@ip-172-31-39-182:/# docker psdock
docker: unknown command: docker psdock

Run 'docker --help' for more information
root@ip-172-31-39-182:/#
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED              STATUS              PORTS                                                                                                           NAMES
a800fb0e6d7c   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   About a minute ago   Up About a minute   8080/tcp, 0.0.0.0:80->80/tcp, [::]:80->80/tcp, 50000/tcp                                                        romantic_lewin
bc684af40e16   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   2 minutes ago        Up 2 minutes        8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   9 minutes ago        Up 9 minutes        0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   22 minutes ago       Up 22 minutes       0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker pull srinfotech
Using default tag: latest
Error response from daemon: pull access denied for srinfotech, repository does not exist or may require 'docker login': denied: requested access to the resource is denied
root@ip-172-31-39-182:/# docker pull nginx
Using default tag: latest
latest: Pulling from library/nginx
dad67da3f26b: Pull complete
4eb3a9835b30: Pull complete
021db26e13de: Pull complete
397cc88dcd41: Pull complete
5f4a88bd8474: Pull complete
66467f827546: Pull complete
f05e87039331: Pull complete
Digest: sha256:dc53c8f25a10f9109190ed5b59bda2d707a3bde0e45857ce9e1efaa32ff9cbc1
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest
root@ip-172-31-39-182:/# docker images
REPOSITORY        TAG       IMAGE ID       CREATED        SIZE
jenkins/jenkins   jdk21     52e1941f479f   21 hours ago   471MB
nginx             latest    9a9a9fd723f1   2 days ago     192MB
root@ip-172-31-39-182:/# docker run -d -p 80:80 nginx:latest
78f28d3d450fa094d496e22de149de21141ffd1e884772251922121a7b40422d
docker: Error response from daemon: failed to set up container networking: driver failed programming external connectivity on endpoint interesting_mclaren (f76b2b0d8ace4755840ce6f55c5da9f57bfed6e0f29dd8a41991b31217fc3f6a): Bind for 0.0.0.0:80 failed: port is already allocated

Run 'docker run --help' for more information
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
a800fb0e6d7c   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   10 minutes ago   Up 10 minutes   8080/tcp, 0.0.0.0:80->80/tcp, [::]:80->80/tcp, 50000/tcp                                                        romantic_lewin
bc684af40e16   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   11 minutes ago   Up 11 minutes   8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   18 minutes ago   Up 18 minutes   0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   31 minutes ago   Up 31 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker stop a800fb0e6d7c
a800fb0e6d7c
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
bc684af40e16   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   12 minutes ago   Up 12 minutes   8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   19 minutes ago   Up 19 minutes   0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   31 minutes ago   Up 31 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker run -d -p 80:80 nginx:latest
585b90814ed4871098000ddaf38376502a490bc2f38bfe625d47a3ddd7f0c85f
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
585b90814ed4   nginx:latest            "/docker-entrypoint.…"   9 seconds ago    Up 9 seconds    0.0.0.0:80->80/tcp, [::]:80->80/tcp                                                                             festive_euler
bc684af40e16   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   12 minutes ago   Up 12 minutes   8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   19 minutes ago   Up 19 minutes   0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   32 minutes ago   Up 32 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker images
REPOSITORY        TAG       IMAGE ID       CREATED        SIZE
jenkins/jenkins   jdk21     52e1941f479f   21 hours ago   471MB
nginx             latest    9a9a9fd723f1   2 days ago     192MB
root@ip-172-31-39-182:/# docker image tag nginx srinfotech7358/SrInfotechnginx:latest
Error parsing reference: "srinfotech7358/SrInfotechnginx:latest" is not a valid repository/tag: invalid reference format: repository name (srinfotech7358/SrInfotechnginx) must be lowercase
root@ip-172-31-39-182:/# docker image tag nginx srinfotech7358/srinfotechnginx:latest
root@ip-172-31-39-182:/# docker images
REPOSITORY                       TAG       IMAGE ID       CREATED        SIZE
jenkins/jenkins                  jdk21     52e1941f479f   21 hours ago   471MB
nginx                            latest    9a9a9fd723f1   2 days ago     192MB
srinfotech7358/srinfotechnginx   latest    9a9a9fd723f1   2 days ago     192MB
root@ip-172-31-39-182:/# docker login -u srinfotech7358

i Info → A Personal Access Token (PAT) can be used instead.
         To create a PAT, visit https://app.docker.com/settings


Password:

WARNING! Your credentials are stored unencrypted in '/root/.docker/config.json'.
Configure a credential helper to remove this warning. See
https://docs.docker.com/go/credential-store/

Login Succeeded
root@ip-172-31-39-182:/# docker push srinfotech7358/srinfotechnginx
Using default tag: latest
The push refers to repository [docker.io/srinfotech7358/srinfotechnginx]
cd38dca3d982: Mounted from library/nginx
d35594dd7e6d: Mounted from library/nginx
126eaee18409: Mounted from library/nginx
6380429cac56: Mounted from library/nginx
13fcb2d303e8: Mounted from library/nginx
151f9feea563: Mounted from library/nginx
7fb72a7d1a8e: Mounted from library/nginx
latest: digest: sha256:3004321c732af3becb9dc247f5e8926faba9186aa67960e15767996abcec588b size: 1778
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
585b90814ed4   nginx:latest            "/docker-entrypoint.…"   10 minutes ago   Up 10 minutes   0.0.0.0:80->80/tcp, [::]:80->80/tcp                                                                             festive_euler
bc684af40e16   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   22 minutes ago   Up 22 minutes   8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   29 minutes ago   Up 29 minutes   0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   42 minutes ago   Up 42 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker stop 585b90814ed4
585b90814ed4
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
bc684af40e16   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   23 minutes ago   Up 23 minutes   8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   30 minutes ago   Up 30 minutes   0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   42 minutes ago   Up 42 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker run -d -p 80:80 srinfotech7358/srinfotechnginx:latest
9f5173c50d14631bd31c8270f79a45db441e8c66db5b730dbb7197de65594c20
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
9f5173c50d14   srinfotech7358/srinfotechnginx:latest   "/docker-entrypoint.…"   9 seconds ago    Up 8 seconds    0.0.0.0:80->80/tcp, [::]:80->80/tcp                                                                             vibrant_dewdney
bc684af40e16   jenkins/jenkins:jdk21                   "/usr/bin/tini -- /u…"   24 minutes ago   Up 24 minutes   8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21                   "/usr/bin/tini -- /u…"   31 minutes ago   Up 31 minutes   0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21                   "/usr/bin/tini -- /u…"   43 minutes ago   Up 43 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker stop 9f5173c50d14
9f5173c50d14
root@ip-172-31-39-182:/# docker ps
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                                                                                           NAMES
bc684af40e16   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   25 minutes ago   Up 25 minutes   8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   32 minutes ago   Up 32 minutes   0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
aca7ec14bfc5   jenkins/jenkins:jdk21   "/usr/bin/tini -- /u…"   44 minutes ago   Up 44 minutes   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker ps -a
CONTAINER ID   IMAGE                                   COMMAND                  CREATED              STATUS                        PORTS                                                                                                           NAMES
9f5173c50d14   srinfotech7358/srinfotechnginx:latest   "/docker-entrypoint.…"   About a minute ago   Exited (137) 27 seconds ago                                                                                                                   vibrant_dewdney
585b90814ed4   nginx:latest                            "/docker-entrypoint.…"   12 minutes ago       Exited (0) 2 minutes ago                                                                                                                      festive_euler
78f28d3d450f   nginx:latest                            "/docker-entrypoint.…"   13 minutes ago       Created                                                                                                                                       interesting_mclaren
a800fb0e6d7c   jenkins/jenkins:jdk21                   "/usr/bin/tini -- /u…"   23 minutes ago       Exited (143) 13 minutes ago                                                                                                                   romantic_lewin
bc684af40e16   jenkins/jenkins:jdk21                   "/usr/bin/tini -- /u…"   25 minutes ago       Up 25 minutes                 8080/tcp, 50000/tcp, 0.0.0.0:8585->8585/tcp, [::]:8585->8585/tcp                                                romantic_buck
601ef30a9a97   jenkins/jenkins:jdk21                   "/usr/bin/tini -- /u…"   32 minutes ago       Up 32 minutes                 0.0.0.0:5001->5001/tcp, [::]:5001->5001/tcp, 8080/tcp, 0.0.0.0:8081->8081/tcp, [::]:8081->8081/tcp, 50000/tcp   frosty_pare
1b6159a409c3   jenkins/jenkins:jdk21                   "/usr/bin/tini -- /u…"   33 minutes ago       Created                                                                                                                                       unruffled_pare
aca7ec14bfc5   jenkins/jenkins:jdk21                   "/usr/bin/tini -- /u…"   44 minutes ago       Up 44 minutes                 0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp, 0.0.0.0:8080->8080/tcp, [::]:8080->8080/tcp, 50000/tcp             festive_tharp
root@ip-172-31-39-182:/# docker start 9f5173c50d14
9f5173c50d14
root@ip-172-31-39-182:/# Read from remote host ec2-35-155-150-89.us-west-2.compute.amazonaws.com: Connection reset by peer
Connection to ec2-35-155-150-89.us-west-2.compute.amazonaws.com closed.
client_loop: send disconnect: Connection reset by peer


Usefull commands:
===============

>docker --version

>docker info

>docker pull <imagename>

>docker pull ubuntu =docker pull ubuntu:latest

>docker images

>docker run -d ubuntu

>docker ps -aq

>docker rmi <imagenname>

>docker run -d -p 8080:8080 -p 5000:5000 jenkins/jenkins:jdk21

>docker exec -it aca7ec14bfc5 /bin/bash     --->inside the container comamnd

>docker run -d -p 8080:8080 -p 5000:5000 jenkins/jenkins:jdk21

>ctrl+pq or exit

>docker image tag nginx srinfotech7358/srinfotechnginx:latest




30/06/2025::
===============


Dockerfile Introduction::
=================

A Dockerfile is a script containing a series of instructions on how to build a Docker image. It defines the environment and application setup, including dependencies, configurations, and the necessary steps to get your application running in a container.

dockerfile is a text file, and it have set up of all instructiuons

https://docs.docker.com/get-started/docker-concepts/building-images/writing-a-dockerfile/


Dockerfile::dockerfile is text file, and it have set up of all instructiuons

FROM nginx or ubuntu or 

LABEL "AUthor =nagaraju@gamil.com"

RUN apt update && apt-get install jenkins -y

COPY . .  ----src destnations

ADD  . . -----src destinatuion

CMD ["echo",".jar"]

ENTRYPOINT ["echo", "war"]

EXPOSE 8080,8085

ENV APP_HOME ="Ifocus SOlutions pvt ltd"

WORKDIR $APP_HOME /app

VOLUME 

Key Components of a Dockerfile:
==========================

FROM: Specifies the base image for the Docker image you're creating.

FROM ubuntu:20.04

RUN: Executes commands inside the container, often used to install dependencies.

RUN apt-get update && apt-get install -y python3

COPY or ADD: Copies files from your local machine into the container.

COPY . /app

WORKDIR: Sets the working directory for any subsequent commands in the Dockerfile.


WORKDIR /app

CMD: Specifies the command to run when a container is started from the image.

CMD ["python3", "app.py"]

EXPOSE: Defines the network ports the container will listen on at runtime.

EXPOSE 8080

ENV: Sets environment variables inside the container.
ENV APP_ENV=production
CMD & ENTRPOINT can be executed starting of the container

CMD & ENTRYPOINT Different::
===========================
--use CMD you can change the value but ENTRYPOINT not possible to change the value at the starting of the container
--CMD you can change the argument value 
--ENTRYPOINT can’t change the argument value

CMD ["echo",".jar"]
ENTRYPOINT ["echo", "war"]

CMD/ENTRYPOINT ====should have something which runs till your app is alive

Note::
=======
life time of your container -->time which your cmd/entrypont is alive

Example Dockerfile:::
==========
Here’s a simple Dockerfile example that builds a Python web app:

# Use an official Python runtime as the base image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container
COPY . /app

# Install the required dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port the app runs on
EXPOSE 5000

# Define the command to run the application
CMD ["python", "app.py"]

Building and Running a Docker Image:
Once you’ve written your Dockerfile, you can build and run it using Docker commands:

Build the Docker image:

>docker build -t my-python-app .

Run the container:
>docker run -d -p 8080:8080 my-python-app

A **Dockerfile** is a script containing a series of instructions on how to build a Docker image. It defines the environment and application setup, including dependencies, configurations, and the necessary steps to get your application running in a container. Essentially, it's the blueprint for creating Docker images.

### Key Components of a Dockerfile:
1. **FROM**: Specifies the base image for the Docker image you're creating.
   ```dockerfile
   FROM ubuntu:20.04
   ```

2. **RUN**: Executes commands inside the container, often used to install dependencies.
   ```dockerfile
   RUN apt-get update && apt-get install -y python3
   ```

3. **COPY** or **ADD**: Copies files from your local machine into the container.
   ```dockerfile
   COPY . /app
   ```

4. **WORKDIR**: Sets the working directory for any subsequent commands in the Dockerfile.
   ```dockerfile
   WORKDIR /app
   ```

5. **CMD**: Specifies the command to run when a container is started from the image.
   ```dockerfile
   CMD ["python3", "app.py"]
   ```

6. **EXPOSE**: Defines the network ports the container will listen on at runtime.
   ```dockerfile
   EXPOSE 8080
   ```

7. **ENV**: Sets environment variables inside the container.
   ```dockerfile
   ENV APP_ENV=production
   ```

### Example Dockerfile
Here’s a simple Dockerfile example that builds a Python web app:

```dockerfile
# Use an official Python runtime as the base image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container
COPY . /app

# Install the required dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port the app runs on
EXPOSE 5000

# Define the command to run the application
CMD ["python", "app.py"]
```

### Building and Running a Docker Image:
Once you’ve written your Dockerfile, you can build and run it using Docker commands:

1. **Build the Docker image**:
   ```bash
   docker build -t my-python-app .
   ```

2. **Run the container**:
   ```bash
   docker run -p 5000:5000 my-python-app
   ```

The Dockerfile streamlines the process of creating consistent and reproducible environments, making it easier to deploy applications across different systems.


Please try Below Example on Docker file:
============================================

https://docs.docker.com/get-started/workshop/02_our_app/




03/07/2025::
=================


Network Types in Docker:
============================

•	bridge: Default network for containers on the same host.
•	host: The container shares the host’s networking stack.
•	overlay: Used for multi-host networking (requires Docker Swarm).
•	none: No network connectivity is assigned to the container.
•	>bridge network is used for single node communication
•	>overlay network is used for multi node communication
•	---Kubernetes/swarm are used to communicate 2 containers in docker that’s like orchestration
macvlan network:: may be used to give containers across different hosts unique, routable IP addresses in a larger network
IPVLAN:Containers share the host’s MAC address but have individual IP addresses.

create my own network ::
=========================
> docker network create my_custom_network

![image](https://github.com/user-attachments/assets/43dbaed8-eb30-45ad-8df3-6cd9f1a3d063)

Created my own network - my_custom_network
![image](https://github.com/user-attachments/assets/a2136223-4a9a-48bc-b884-3e64a57268d5)

Run Containers on the Custom Network::
=================
>docker run -d --name container1 --network my_custom_network nginx

![image](https://github.com/user-attachments/assets/0f65c683-0ef5-4415-9413-41a46735a633)

>docker run -d --name container2 --network my_custom_network redis


![image](https://github.com/user-attachments/assets/0a4811c8-24cf-400a-93f9-e72196d504a5)

In this example:
•	container1 will run an Nginx container.
•	container2 will run a Redis container.

Both containers are connected to the my_custom_network.

Inspect the Network::
=================
To view detailed information about a network (like connected containers and settings), use the docker network inspect command:
>docker ps
>docker network ls
> docker network inspect my_custom_network

![image](https://github.com/user-attachments/assets/367d1d82-51e3-43fa-88c0-5a8414c73688)

Connect a Container to a Network:
==================
> docker network connect my_custom_network container_name
Disconnect a Container from a Network:
> docker network disconnect my_custom_network container_name
Remove a Docker Network::
>docker network rm my_custom_network
Note that the network must be unused by any containers before it can be removed.

A common use case for Docker networks is to isolate different applications or microservices, ensuring that containers in one application cannot easily communicate with containers in another. This helps you maintain security and control over how containers interact with each other.

USE CASE::
======================

--default network bridge can only ping throw ip address not container name
--our own network bridge(mybridge) able to ping both ip address and container name that’s advantage of network create.


---Kubernetes/swarm are used to communicate 2 containers in docker that’s like orchestration
--if you create your own bridge network the advantage is you can able to resolved the any issues using container name not only ipaddress but by default using you can able to resolved the issues by ipaddress.

>bridge network is used for single node communication
>overlay network is used for multi node communication


Docker Swarm::
===================

Docker and Docker Swarm are both tools used to manage containers, but they serve different purposes and have different features. 


![image](https://github.com/user-attachments/assets/a7dc1fa3-6551-44cf-b954-7e411141b87e)


Docker::
===========

Docker is a platform that allows you to create, deploy, and run applications inside containers. Containers are lightweight, portable, and ensure that the application works the same regardless of where it's deployed, making Docker a powerful tool for developing, testing, and deploying applications.


Key Features of Docker:
=======================
•	Containerization: Docker encapsulates applications and their dependencies into containers, ensuring consistency across environments (e.g., development, staging, production).
•	Images and Containers: Docker uses images to define the environment for an application. Containers are instances of those images.
•	Docker Hub: Docker Hub is a cloud-based registry where you can find pre-built images or upload your own.
•	Portability: Docker containers can run on any system with Docker installed, from your laptop to a cloud server.
•	Isolation: Containers are isolated from the host system, so they don’t interfere with other processes or systems.

Common Docker Commands:
===================
•	Build an Image: docker build -t my-image .
•	Run a Container: docker run -d --name my-container my-image
•	List Containers: docker ps
•	Stop a Container: docker stop my-container
•	Remove a Container: docker rm my-container
•	List Images: docker images

Docker Swarm::
==================

Docker Swarm is a clustering and orchestration tool for Docker containers. It allows you to deploy and manage multiple containers across multiple Docker hosts (machines), forming a swarm. This means that you can treat a collection of Docker hosts as a single virtual host and manage them as one.
Docker Swarm makes it easier to scale, deploy, and maintain containerized applications in production environments. It provides high availability, fault tolerance, and easy scaling of applications across multiple machines.


Docker SWARM Overview::
=====================
- this is Docker Inc's Container Orchestration Platform
- it only supports managing Docker containerized application workloads
- it is pretty easy to install and learn
- can be installed on a laptop with pretty basic configuation as well as it is very light weight
- good for POC or learning purpose
- not production grade


Key Concepts in Docker Swarm:
===============================
•	Node: A machine (physical or virtual) running Docker that is part of the Swarm cluster. There are two types of nodes:
o	Manager Node: Manages the cluster and orchestrates services.
o	Worker Node: Runs the actual containers based on instructions from manager nodes.
•	Service: A service is a description of the tasks (containers) you want to run. When you define a service, Docker Swarm ensures that the desired number of replicas of that service are running at all times.
•	Task: A task is a running container in the context of a service. Each task runs a container that is part of a service.

Docker vs Docker Swarm::
============================
•	Docker is used to build and run containers on a single machine, whereas Docker Swarm extends Docker to manage containers across a cluster of machines.
•	Docker Swarm provides orchestration features such as load balancing, scaling, and high availability, which are not available in basic Docker.
•	Docker Swarm is built into Docker, making it easier to set up and use compared to other container orchestration systems like Kubernetes.


I have created 3 ubuntu machines::
================================

1.Manager Node
2.Worker Node1
3. Worker Node2

![image](https://github.com/user-attachments/assets/1c3827ee-7df0-4063-b36e-51345ef08afd)


![image](https://github.com/user-attachments/assets/8d70d3eb-1df0-46a0-bbae-fa9474112b8f)

>docker swarm init runs on master
>docker swarm join runs on node

> docker swarm join --token SWMTKN-1-33cj3h7mhtq98iy5aifyy9s1cdqnzh4jgl3rdgdez0vbfx8fnc-bu27q63wt2i7qfgkh0r07o85o 172.31.24.64:2377

![image](https://github.com/user-attachments/assets/c3434137-924b-4ea7-9a3f-24f188d3d19a)

![image](https://github.com/user-attachments/assets/015201ed-aea1-461f-90bc-08c1d78fae7b)

![image](https://github.com/user-attachments/assets/06424e51-1f9b-46e3-89af-80062ccb2f26)

>once initialize the swarm it will automatically created overlay network

![image](https://github.com/user-attachments/assets/d19378c2-01c9-4698-ad1d-c8af6aff1a55)


create our own overlay network ::
==========================

>docker network create –d overlay qt-overlay

![image](https://github.com/user-attachments/assets/84319ff3-e569-40c5-bdf6-69634bf65484)

> docker network create -d overlay qt-overlay
>docker node ls

![image](https://github.com/user-attachments/assets/3fb48730-74d2-4e65-ac80-dce537b2438a)

![image](https://github.com/user-attachments/assets/c545c853-157b-484f-8b7b-e3c81236d142)

create service under the overlay network::
========================

> docker service create --name my-web-service --replicas 3 -p 80:80 nginx
>docker service ls
>docker node ls

--docker always maintain --replicas 3 means 3 containers by default if for example 1 container die docker automatically create container automatically this is main use of services with docker

docker swarm:: multi containarization for your applications

Docker Swarm is a built-in container orchestration tool that allows you to manage a cluster of Docker hosts as a single entity

in any cloud we have docker /container services lke

1.AWS --->ECS ----elastic conatienr services
2.Azure---->ACS  ----Azure contaienr services
3.Kuberneties---->EKS  ---Elsatic kuberneties services


04/07/2025::
=================


Docker Flow

![image](https://github.com/user-attachments/assets/29c7ef27-30c5-4b2a-b22a-b0fa6cfba2e8)



Docker compose::
=====================

Docker Compose is a tool for defining and running multi-container Docker applications. With a docker-compose.yml file, you can configure your application’s services, networks, and volumes, and then start them all with a single command.
Below, I'll explain how to create a docker-compose.yml file and walk you through an example that demonstrates its use.
version: "3"  # Specify the version of Docker Compose

services:
  <service_name>:  # Define your services (containers)
    image: <image_name>  # The Docker image to use (can be local or from Docker Hub)
    build: <path_to_dockerfile>  # Path to the Dockerfile if you need to build the image
    container_name: <container_name>  # Optionally define a container name
    ports:  # Map container ports to host ports
      - "<host_port>:<container_port>"
    volumes:  # Mount volumes (directories or files)
      - <host_directory>:<container_directory>
    environment:  # Set environment variables
      - <key>=<value>
    depends_on:  # Define dependencies between services
      - <another_service>
    networks:  # Specify networks to connect to
      - <network_name>

networks:
  <network_name>:  # Define custom networks
    driver: bridge  # Optional: can be "bridge", "host", or "none"

volumes:
  <volume_name>:  # Define named volumes for persistent data

Explanation of the docker-compose.yml Example:
1.	Version: Specifies the version of the Docker Compose file format to use. In this case, 3.8.
2.	Services:
o	web: This is the service for your Node.js application.
	image: Specifies the base image to use (node:18-alpine).
	working_dir: Sets the working directory inside the container.
	volumes: Mounts the current directory (.) to /app inside the container so your application code is accessible to the container.
	ports: Maps port 3000 on the host to port 3000 inside the container.
	environment: Sets environment variables like NODE_ENV and the database connection information (DB_HOST=db).
	depends_on: Ensures the db service is started before the web service.
o	db: This is the service for your MySQL database.
	image: Specifies the MySQL version to use (mysql:8.0).
	environment: Sets environment variables such as the MySQL root password, database name, and user credentials.
	volumes: Mounts a named volume (db-data) to persist MySQL data between container restarts.
	ports: Exposes port 3306 for MySQL to allow communication between containers or with the host.
3.	Volumes: Defines a named volume (db-data) to persist the database data outside of the container.


docker-compose.yml::
=====================

version: '3.8'

services:
  web:
    image: node:18-alpine  # Use the official Node.js image
    container_name: node-app
    working_dir: /app
    volumes:
      - .:/app  # Mount the current directory to /app in the container
    ports:
      - "3000:3000"  # Expose port 3000 on the host and map it to port 3000 in the container
    environment:
      - NODE_ENV=development
      - DB_HOST=db  # Reference the db service as the hostname
    depends_on:
      - db  # Ensure the db service starts first

  db:
    image: mysql:8.0  # Use the official MySQL image
    container_name: mysql-db
    environment:
      MYSQL_ROOT_PASSWORD: rootpassword
      MYSQL_DATABASE: mydb
      MYSQL_USER: user
      MYSQL_PASSWORD: password
    volumes:
      - db-data:/var/lib/mysql  # Mount a volume for persistent data
    ports:
      - "3306:3306"  # Expose port 3306 for MySQL

volumes:
  db-data:  # Define a volume for MySQL data persistence

> docker compose up -d

>docker exec -it bbeebd8d5ca2 /bin/bash

> mysql -u root -p

> SHOW DATABASES;

CREATE DATABASE SRINFOTECH;
USE SRINFOTECH;

CREATE TABLE SRINFOTECHTABLE ( id INT NOT NULL, name VARCHAR(250) NOT NULL, cource VARCHAR(100) NOT NULL, city VARCHAR(200) NOT NULL, PRIMARY KEY(id) );

INSERT INTO SRINFOTECHTABLE VALUES ( 1, "veeresh", "AWSDEVOPS","Hyderabad" );

INSERT INTO SRINFOTECHTABLE VALUES ( 2, "laxmikanth", "AWSDEVOPSTraining","Bangalour" );

INSERT INTO SRINFOTECHTABLE VALUES ( 1, "Rawali", "AWSDEVOPSFullStack","Chennai" );

SELECT * FROM SRINFOTECHTABLE;


Use Cases for Docker Compose:
•	Multi-container applications: Perfect for web applications that rely on more than one service (e.g., database, caching, backend).
•	Development environments: Provides a consistent environment that can be easily replicated across different machines.
•	Testing and CI/CD: Can be used to quickly spin up environments for testing or continuous integration/deployment pipelines



Docker Compose Quickstart::
============================

please try to practice below example for docker compose 

https://docs.docker.com/compose/gettingstarted/


![image](https://github.com/user-attachments/assets/8683a557-4a34-42a1-93ee-ca1cbf78fdfa)


Example2 Dockerfile::
===================

https://github.com/srinfotech7358/spring-ms.git

Please clone this project in ubuntu machines

root@ip-172-31-20-86:~# git clone https://github.com/srinfotech7358/spring-ms.git

![image](https://github.com/user-attachments/assets/188db6f2-c5b5-419d-8824-0b9b9c6728ee)

root@ip-172-31-20-86:~# cd spring-ms/
root@ip-172-31-20-86:~/spring-ms# ls
Dockerfile  azure-pipeline.yml  azure-pipelines.yml  deploy.yaml  pom.xml  src
root@ip-172-31-20-86:~/spring-ms#

Build Image::
============
root@ip-172-31-20-86:~/spring-ms# docker image build -t springmyapp .
[+] Building 0.4s (12/12) FINISHED                                                                                      docker:default
 => [internal] load build definition from Dockerfile                                                                              0.0s
 => => transferring dockerfile: 256B                                                                                              0.0s
 => WARN: FromAsCasing: 'as' and 'FROM' keywords' casing do not match (line 1)                                                    0.0s
 => [internal] load metadata for registry.access.redhat.com/ubi8/openjdk-11:latest                                                0.3s
 => [internal] load metadata for docker.io/library/maven:3.6.3-jdk-11                                                             0.1s
 => [auth] library/maven:pull token for registry-1.docker.io                                                                      0.0s
 => [internal] load .dockerignore                                                                                                 0.0s
 => => transferring context: 2B                                                                                                   0.0s
 => [internal] load build context                                                                                                 0.0s
 => => transferring context: 2.76kB                                                                                               0.0s
 => [stage-1 1/2] FROM registry.access.redhat.com/ubi8/openjdk-11:latest@sha256:28b35eea470174a39befd8eb9250a3276b79a4f6e7dac787  0.0s
 => [stage1 1/3] FROM docker.io/library/maven:3.6.3-jdk-11@sha256:1d29ccf46ef2a5e64f7de3d79a63f9bcffb4dc56be0ae3daed5ca5542b38aa  0.0s
 => CACHED [stage1 2/3] COPY . .                                                                                                  0.0s
 => CACHED [stage1 3/3] RUN mvn clean package                                                                                     0.0s
 => CACHED [stage-1 2/2] COPY --from=stage1 target/*.jar app.jar                                                                  0.0s
 => exporting to image                                                                                                            0.0s
 => => exporting layers                                                                                                           0.0s
 => => writing image sha256:bdbbb4bbe700af425032e6a27d6909e2906677fbffce9b833d596e3f37082479                                      0.0s
 => => naming to docker.io/library/springmyapp                                                                                    0.0s

 1 warning found (use docker --debug to expand):
 - FromAsCasing: 'as' and 'FROM' keywords' casing do not match (line 1)
root@ip-172-31-20-86:~/spring-ms#

![image](https://github.com/user-attachments/assets/44c6ba1e-7322-436d-af30-4606cb484283)

create container::
===============

root@ip-172-31-20-86:~/spring-ms# docker images
REPOSITORY                  TAG       IMAGE ID       CREATED        SIZE
spring                      latest    bdbbb4bbe700   9 hours ago    410MB
springmyapp                 latest    bdbbb4bbe700   9 hours ago    410MB
srinu7358/spring-03042025   latest    bdbbb4bbe700   9 hours ago    410MB
allinstructions             latest    c2993e54968d   9 hours ago    1.17GB
<none>                      <none>    805cbec82269   9 hours ago    1.17GB
testmyownimage              latest    621f509fde33   10 hours ago   1.1GB
ifocus                      latest    381bfb89fb02   10 hours ago   1.1GB
srinu7358/ifocus-myapp      latest    381bfb89fb02   10 hours ago   1.1GB
root@ip-172-31-20-86:~/spring-ms# docker run -d -p 8081:8081 springmyapp:latest
17ac78f05de4abdca3d46972e63f29c897a011d732ca3e76e7c1ef2158af10b1
root@ip-172-31-20-86:~/spring-ms#

![image](https://github.com/user-attachments/assets/d0132046-021c-46b7-9259-75382dc155fb)

![image](https://github.com/user-attachments/assets/b9064110-355c-4619-adf5-fb9fac875b6f)

Image formate::
============

<registoryname>/repositoryname:<imagetag>
Docker.io            username/reponame  ::latest

[docker.io/srinu7358/ifocus-myapp] :latest  ---->image formate

docker.io -----registry name  ----docekr hub

srinu7358 ----repository username

ifocus-myapp ---image name

>docker container run –d –p 8080:8080 springmyapp:1.0
-d --> detached mode
-p  -->mappimg a port
8080: host port
8080: container port
springmyapp:: image name
1.0:: tag name

Expected 
http://54.162.108.91:8080/


![image](https://github.com/user-attachments/assets/3f90a7ca-b7a7-4d5d-ac7a-0d8a24346518)


Usefull commands::
====================

>docker compose up

sudo apt-get install docker-compose-plugin
>docker image tag srinfotechmyapp srinfotech7358/myapp:latest

>docker.io/library/hello-world:latest

docker.io--->registry name
library  -->username-->docker hub username--

Image formate is

registry name/repositoryusername/imagename:tagname

docker -io/srinfotech7358/myapp:latest





07/07/2025::
================

Docker SWARM Overview::
=============================

1.this is Docker Inc's Container Orchestration Platform
2.it only supports managing Docker containerized application workloads
3.it is pretty easy to install and learn
4.can be installed on a laptop with pretty basic configuation as well as it is very light weight
5.good for POC or learning purpose
6.not production grade

Kubernetes Overview::
========================


Kubernetes (often abbreviated as K8s) is an open-source container orchestration platform designed to automate the deployment, scaling, and management of containerized applications. Originally developed by Google.


![image](https://github.com/user-attachments/assets/6f78888e-d2cd-469b-9f17-14d79c7458ce)


free and opensource container orchestration platform developed by Google along with many open source contributors

it is production grade

free for personal and commercial use

as it is opensource, we won't get support from Google

only supports command line interface (CLI)

doesn't support web console

Kubernetes does provide some basic Dashboard but it is considered a security vulnerability, hence no one uses the Kubernetes Dashboard

Rancher is opensource webconsole for Google Kubernetes

supports inbuilt monitoring features

it can check the health of our application, when it finds your application is not responding, it can repair it or replace it with another good healthy instance of your application
it supports inbuilt load-balancing
Master ---Management --(Orchestration) Node machine (minion) --workers (containers)

POD ---the smallest unit, mainatained one or more containers

YAML --key-value paires

1.Container Orchestration: Kubernetes helps you manage multiple containers, ensuring that they run efficiently and reliably across many servers.

2.Scaling: Kubernetes can automatically scale your applications up or down based on demand, making it easier to handle varying workloads.

3.Load Balancing: It can distribute network traffic to different containers, ensuring that applications remain responsive even under heavy loads.

4.Self-Healing: If a container crashes or stops working, Kubernetes can automatically restart or replace it, ensuring the application stays available.

5.Automated Deployment and Rollback: Kubernetes can automate the process of deploying new versions of an application, and if something goes wrong, it can roll back to a previous version.

6.Storage Management: Kubernetes can automatically mount the storage resources you need for your applications, making it easier to manage persistent data.

In short, Kubernetes is designed to make it easier to manage applications at scale in a way that is highly automated, reliable, and efficient. It’s widely used in DevOps platform

Cluster:: collection of nodes with a single responsibility

All the nodes in that cluster do same process, same type of work can will do collection of nodes in cluster

Cluster::
a cluster might refer to a set of virtual machines or containers working together for a specific application or service.


Kubernetes Cluster Components:
1.Master Node (Control Plane): The Master Node is the brain of the Kubernetes cluster. It manages the cluster and makes decisions about scheduling, scaling, and maintaining the health of the application. The control plane consists of several key components:

1.API Server::
The API server exposes the Kubernetes API, which is used to interact with the cluster.

2.Scheduler::
The scheduler assigns work (pods) to available worker nodes.

3.Controller Manager: :
Ensures that the desired state of the system is maintained, such as ensuring that the correct number of pods are running.

4.etcd:
A distributed key-value store used to store all cluster data, including the state of the system (like deployed pods, config maps, and secrets).

Worker Nodes (Minions):
o The Worker Nodes are responsible for running the actual application workloads. These nodes host the pods, which are the smallest deployable units in Kubernetes. A worker node typically runs:

1.Kubelet: An agent that ensures the containers in the pods are running and healthy.

2.Kube Proxy: A network proxy that maintains network rules for pod communication.

3.Container Runtime: The software responsible for running containers (e.g., Docker, containerd).

4.Pods::

A pod is the smallest unit of execution in Kubernetes and can contain one or more containers that share resources such as networking and storage. Pods are always deployed in a Kubernetes cluster and are managed by the control plane.



08/07/2025::
===============

Services:
===============
A service in Kubernetes is a way to expose an application running in a pod to other pods or external users. It ensures that network communication between pods is reliable, even as pods are dynamically created or destroyed.

1.Pod is a smallest component in kubernetes 

2.In docker smallest component --  > container

3.in kuberneties we will create pods and inside the pods containers are running.

4.one pod speak with other pod using id address(kube-proxy)

5.every pod has ip address


![image](https://github.com/user-attachments/assets/2706e391-c562-4c6c-81b3-0405872de65d)


Above picture directly using pods without using services and if ipaddress no longer available our application is not worked. pods communication throw ip address right so it has a problem to resolved the this problem services is come to the picture.

With Services::
==================

![image](https://github.com/user-attachments/assets/697aa9c5-fad7-4683-9281-f8adba328d89)


Services –logical entity and maintain ip address


Basically kubernetes is used for maintain containers


Kubeadm::
============
bootstraps a cluster. It’s designed to be a simple way for new users to build clusters (more detail on this is in a later chapter).

Kubectl::
===========
is a tool for interacting with your existing cluster.

Kubelet: 
============
An agent that ensures the containers in the pods are running and check healthy.


How to Install Kubernetes Cluster on Ubuntu 22.04::
=====================================================

Please follow the below link steps to configured the Kubernetes Master and Workers 

https://www.linuxtechi.com/install-kubernetes-on-ubuntu-22-04/


>kubectl get nodes


root@k8smaster:~# kubectl get nodes
NAME         STATUS   ROLES           AGE   VERSION
k8smaster    Ready    control-plane   11h   v1.28.15
k8sworker1   Ready    <none>          11h   v1.28.15
k8sworker2   Ready    <none>          11h   v1.28.15


![image](https://github.com/user-attachments/assets/bdbf060a-bdf4-41d3-81c3-b4ac9931fc18)





10/07/2025::
=============

Docker Install link::
=======================

Make sure we should install the Docker in all the machines 

https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-22-04

root@k8smaster:~# docker --version

Docker version 28.3.2, build 578ccf6

root@k8smaster:~#

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9ca614f3-f4cf-4339-bbd1-aac6a45b0efc" />


Clone the Project (docker-Java-kubernetes-project) :::
====================================================

>git clone https://github.com/ifocus7358/docker-Java-kubernetes-project.git

root@ip-172-31-36-154:~# git clone https://github.com/ifocus7358/docker-Java-kubernetes-project.git
Cloning into 'docker-Java-kubernetes-project'...
remote: Enumerating objects: 156, done.
remote: Counting objects: 100% (42/42), done.
remote: Compressing objects: 100% (32/32), done.
remote: Total 156 (delta 27), reused 10 (delta 10), pack-reused 114 (from 1)
Receiving objects: 100% (156/156), 27.40 KiB | 9.13 MiB/s, done.
Resolving deltas: 100% (35/35), done.

Build the image::
============

root@ip-172-31-36-154:~# ls

docker-Java-kubernetes-project 

root@ip-172-31-36-154:~# cd docker-Java-kubernetes-project/

root@ip-172-31-36-154:~/docker-Java-kubernetes-project# ls

README.md  kubernetes  productcatalogue  shopfront  stockmanager
root@ip-172-31-36-154:~/docker-Java-kubernetes-project# cd kubernetes/

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# ls

productcatalogue-service.yaml  shopfront-service.yaml  stockmanager-service.yaml
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# cd ..

root@ip-172-31-36-154:~/docker-Java-kubernetes-project# ls

README.md  kubernetes  productcatalogue  shopfront  stockmanager

root@ip-172-31-36-154:~/docker-Java-kubernetes-project# cd shopfront/

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# ls

Dockerfile  pom.xml  src
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront#

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker image build -t shopfront .


installed maven::
===============

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# mvn -v

Apache Maven 3.8.7

So need to build the source code first it will generate target folder

>mvn clean install

[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  5.598 s
[INFO] Finished at: 2025-04-08T05:52:09Z
[INFO] ------------------------------------------------------------------------



root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# ls

Dockerfile  pom.xml  src  target
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# cd  target/

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront/target# ls

classes  generated-sources  maven-archiver  maven-status  shopfront-0.0.1-SNAPSHOT.jar  shopfront-0.0.1-SNAPSHOT.jar.original
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront/target# ls

classes  generated-sources  maven-archiver  maven-status  shopfront-0.0.1-SNAPSHOT.jar  shopfront-0.0.1-SNAPSHOT.jar.original
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront/target# cd ..
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker build -t shopfront .

[+] Building 8.8s (7/7) FINISHED                                                                                        docker:default
 => [internal] load build definition from Dockerfile                                                                              0.0s
 => => transferring dockerfile: 198B                                                                                              0.0s
 => [internal] load metadata for docker.io/library/openjdk:8-jre                                                                  0.1s
 => [internal] load .dockerignore                                                                                                 0.0s
 => => transferring context: 2B                                                                                                   0.0s
 => [internal] load build context                                                                                                 0.5s
 => => transferring context: 46.10MB                                                                                              0.5s
 => [1/2] FROM docker.io/library/openjdk:8-jre@sha256:667a15e7bc533a90fb39ddb7e5bed63162ac3c13a97e6c698bf4f139f51b7d33            6.1s
 => => resolve docker.io/library/openjdk:8-jre@sha256:667a15e7bc533a90fb39ddb7e5bed63162ac3c13a97e6c698bf4f139f51b7d33            0.0s
 => => sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a 10.88MB / 10.88MB                                  0.3s
 => => sha256:a6a74c7b774e00fd2ec5664e257d344f1b7e69e2a618b1c0678f69719863c5ad 1.58kB / 1.58kB                                    0.0s
 => => sha256:0c14a0e20aa3a19448f6227265c6642571112e9cd9a69b5e7a323df46d1aa835 7.43kB / 7.43kB                                    0.0s
 => => sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165 5.16MB / 5.16MB                                    0.2s
 => => sha256:667a15e7bc533a90fb39ddb7e5bed63162ac3c13a97e6c698bf4f139f51b7d33 1.04kB / 1.04kB                                    0.0s
 => => sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452 55.00MB / 55.00MB                                  1.3s
 => => sha256:8510da692cda60e4746c14dd90905695eade5888e2ad640706a2be9dc42a0224 5.66MB / 5.66MB                                    0.5s
 => => sha256:c34215579d03c1311f4e8cd3525bc03dbbb53d79d8b58e63cce8cdd355356347 211B / 211B                                        0.4s
 => => sha256:73d77b4774a96dfa09076212d5170e977d153ceab60c1ec4312a8f436b91371c 41.42MB / 41.42MB                                  1.2s
 => => extracting sha256:001c52e26ad57e3b25b439ee0052f6692e5c0f2d5d982a00a8819ace5e521452                                         2.7s
 => => extracting sha256:d9d4b9b6e964657da49910b495173d6c4f0d9bc47b3b44273cf82fd32723d165                                         0.2s
 => => extracting sha256:2068746827ec1b043b571e4788693eab7e9b2a95301176512791f8c317a2816a                                         0.3s
 => => extracting sha256:8510da692cda60e4746c14dd90905695eade5888e2ad640706a2be9dc42a0224                                         0.2s
 => => extracting sha256:c34215579d03c1311f4e8cd3525bc03dbbb53d79d8b58e63cce8cdd355356347                                         0.0s
 => => extracting sha256:73d77b4774a96dfa09076212d5170e977d153ceab60c1ec4312a8f436b91371c                                         1.0s
 => [2/2] ADD target/shopfront-0.0.1-SNAPSHOT.jar app.jar                                                                         2.1s
 => exporting to image                                                                                                            0.3s
 => => exporting layers                                                                                                           0.3s
 => => writing image sha256:3ccf19de392942c193c580caabe914257071f0c0b1cb8c8b371d369d5e0630fd                                      0.0s
 => => naming to docker.io/library/shopfront                                                                                      0.0s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker images

REPOSITORY                    TAG       IMAGE ID       CREATED          SIZE
shopfront                     latest    3ccf19de3929   14 seconds ago   320MB
gcr.io/k8s-minikube/kicbase   v0.0.46   e72c4cbe9b29   2 months ago     1.31GB
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker run -d -p 80:80 shopfront

836d8e23016935ac3cd74067bbdb4998dba147ce425d17edafced967b1884233
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker ps

CONTAINER ID   IMAGE                                 COMMAND                  CREATED          STATUS          PORTS                                                                                                                                  NAMES
836d8e230169   shopfront                             "java -Djava.securit…"   6 seconds ago    Up 5 seconds    0.0.0.0:80->80/tcp, [::]:80->80/tcp, 8010/tcp                                                                                          epic_leavitt
ad8f297fbeca   gcr.io/k8s-minikube/kicbase:v0.0.46   "/usr/local/bin/entr…"   27 minutes ago   Up 27 minutes   127.0.0.1:32768->22/tcp, 127.0.0.1:32769->2376/tcp, 127.0.0.1:32770->5000/tcp, 127.0.0.1:32771->8443/tcp, 127.0.0.1:32772->32443/tcp   minikube
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront#

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker images

REPOSITORY                    TAG       IMAGE ID       CREATED         SIZE
shopfront                     latest    3ccf19de3929   3 minutes ago   320MB
gcr.io/k8s-minikube/kicbase   v0.0.46   e72c4cbe9b29   2 months ago    1.31GB
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker ps

CONTAINER ID   IMAGE                                 COMMAND                  CREATED              STATUS              PORTS                                                                                                                                  NAMES
836d8e230169   shopfront                             "java -Djava.securit…"   About a minute ago   Up About a minute   0.0.0.0:80->80/tcp, [::]:80->80/tcp, 8010/tcp                                                                                          epic_leavitt
ad8f297fbeca   gcr.io/k8s-minikube/kicbase:v0.0.46   "/usr/local/bin/entr…"   28 minutes ago       Up 28 minutes       127.0.0.1:32768->22/tcp, 127.0.0.1:32769->2376/tcp, 127.0.0.1:32770->5000/tcp, 127.0.0.1:32771->8443/tcp, 127.0.0.1:32772->32443/tcp   minikube
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker rm 836d8e230169
Error response from daemon: cannot remove container "/epic_leavitt": container is running: stop the container before removing or force remove
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker rm -f 836d8e230169

836d8e230169
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker ps

CONTAINER ID   IMAGE                                 COMMAND                  CREATED          STATUS          PORTS                                                                                                                                  NAMES
ad8f297fbeca   gcr.io/k8s-minikube/kicbase:v0.0.46   "/usr/local/bin/entr…"   29 minutes ago   Up 29 minutes   127.0.0.1:32768->22/tcp, 127.0.0.1:32769->2376/tcp, 127.0.0.1:32770->5000/tcp, 127.0.0.1:32771->8443/tcp, 127.0.0.1:32772->32443/tcp   minikube
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker images

REPOSITORY                    TAG       IMAGE ID       CREATED         SIZE
shopfront                     latest    3ccf19de3929   4 minutes ago   320MB
gcr.io/k8s-minikube/kicbase   v0.0.46   e72c4cbe9b29   2 months ago    1.31GB
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker image tag shopfront srinu7358/shopfront-myapp

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker images

REPOSITORY                    TAG       IMAGE ID       CREATED         SIZE
shopfront                     latest    3ccf19de3929   6 minutes ago   320MB
srinu7358/shopfront-myapp     latest    3ccf19de3929   6 minutes ago   320MB
gcr.io/k8s-minikube/kicbase   v0.0.46   e72c4cbe9b29   2 months ago    1.31GB
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker login -u srinu7358

i Info → A Personal Access Token (PAT) can be used instead.
         To create a PAT, visit https://app.docker.com/settings


Password:

WARNING! Your credentials are stored unencrypted in '/root/.docker/config.json'.
Configure a credential helper to remove this warning. See
https://docs.docker.com/go/credential-store/

Login Succeeded
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker push srinnfotech7358/shopfrontnewapp

Using default tag: latest
The push refers to repository [docker.io/srinu7358/shopfront-myapp]
c54136e18c64: Pushed
1aaddf64804f: Mounted from library/openjdk
990c5138f5d1: Mounted from library/openjdk
5c384ea5f752: Mounted from library/openjdk
293d5db30c9f: Mounted from library/openjdk
03127cdb479b: Mounted from library/openjdk
9c742cd6c7a5: Mounted from library/openjdk
latest: digest: sha256:e027803e479a98c9d1fdcc6d983a6b778b62c2a91dee9bcccfffcb921848b42e size: 1794
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker pull srinu7358/shopfront-myapp:latest

latest: Pulling from srinu7358/shopfront-myapp
Digest: sha256:e027803e479a98c9d1fdcc6d983a6b778b62c2a91dee9bcccfffcb921848b42e
Status: Image is up to date for srinu7358/shopfront-myapp:latest
docker.io/srinu7358/shopfront-myapp:latest
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# docker images

REPOSITORY                    TAG       IMAGE ID       CREATED          SIZE
shopfront                     latest    3ccf19de3929   12 minutes ago   320MB
srinnfotech7358/shopfrontnewapp     latest    3ccf19de3929   12 minutes ago   320MB
gcr.io/k8s-minikube/kicbase   v0.0.46   e72c4cbe9b29   2 months ago     1.31GB
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/shopfront# cd ..

root@ip-172-31-36-154:~/docker-Java-kubernetes-project# ls

README.md  kubernetes  productcatalogue  shopfront  stockmanager
root@ip-172-31-36-154:~/docker-Java-kubernetes-project# Read from remote host ec2-54-174-108-84.compute-1.amazonaws.com: Connection reset by peer
Connection to ec2-54-174-108-84.compute-1.amazonaws.com closed.
client_loop: send disconnect: Connection reset by peer


pushed image to docker hub::
----------------------

![image](https://github.com/user-attachments/assets/4223faf9-b478-4d75-8f4e-7c7017d52e7b)


Please build the stockmanager project and it will generated target/ after build success

[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  5.152 s
[INFO] Finished at: 2025-04-10T04:54:00Z
[INFO] ------------------------------------------------------------------------
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/stockmanager# ls
Dockerfile  build  pom.xml  src  target
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/stockmanager# cd target/
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/stockmanager/target# ls
classes  generated-sources  maven-archiver  maven-status  stockmanager-0.0.1-SNAPSHOT.jar  stockmanager-0.0.1-SNAPSHOT.jar.original


Build the Image::
=================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/stockmanager# docker image build -t stockmanager .


[+] Building 1.1s (8/8) FINISHED                                                                                        docker:default
 => [internal] load build definition from Dockerfile                                                                              0.0s
 => => transferring dockerfile: 201B                                                                                              0.0s
 => [internal] load metadata for docker.io/library/openjdk:8-jre                                                                  0.1s
 => [auth] library/openjdk:pull token for registry-1.docker.io                                                                    0.0s
 => [internal] load .dockerignore                                                                                                 0.0s
 => => transferring context: 2B                                                                                                   0.0s
 => [internal] load build context                                                                                                 0.4s
 => => transferring context: 43.32MB                                                                                              0.4s
 => CACHED [1/2] FROM docker.io/library/openjdk:8-jre@sha256:667a15e7bc533a90fb39ddb7e5bed63162ac3c13a97e6c698bf4f139f51b7d33     0.0s
 => [2/2] ADD target/stockmanager-0.0.1-SNAPSHOT.jar app.jar                                                                      0.2s
 => exporting to image                                                                                                            0.3s
 => => exporting layers                                                                                                           0.3s
 => => writing image sha256:3de0cce0b9d4173e0ab799d4a59b986a841c5e08244b25d0887f1d0a9d496662                                      0.0s
 => => naming to docker.io/library/stockmanager 

Verify the docker images::
=================
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/stockmanager# docker images

REPOSITORY                    TAG       IMAGE ID       CREATED          SIZE
stockmanager                  latest    3de0cce0b9d4   10 seconds ago   317MB
shopfront                     latest    3ccf19de3929   47 hours ago     320MB
srinu7358/shopfront-myapp     latest    3ccf19de3929   47 hours ago     320MB
gcr.io/k8s-minikube/kicbase   v0.0.46   e72c4cbe9b29   2 months ago     1.31GB


 Tag the Image:;
==============

 root@ip-172-31-36-154:~/docker-Java-kubernetes-project/stockmanager# docker image tag stockmanager srinu7358/stockmanager-myapp
 
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/stockmanager# docker images

REPOSITORY                     TAG       IMAGE ID       CREATED              SIZE
stockmanager                   latest    3de0cce0b9d4   About a minute ago   317MB
srinu7358/stockmanager-myapp   latest    3de0cce0b9d4   About a minute ago   317MB
shopfront                      latest    3ccf19de3929   47 hours ago         320MB
srinu7358/shopfront-myapp      latest    3ccf19de3929   47 hours ago         320MB
gcr.io/k8s-minikube/kicbase    v0.0.46   e72c4cbe9b29   2 months ago         1.31GB


Login to DockerHub::
-------------------

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/stockmanager# docker login -u srinu7358


i Info → A Personal Access Token (PAT) can be used instead.
         To create a PAT, visit https://app.docker.com/settings


Password:
Login Succeeded

Pushed image to docker hub::
============================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/stockmanager# docker push srinu7358/stockmanager-myapp

Using default tag: latest
The push refers to repository [docker.io/srinu7358/stockmanager-myapp]
03b73450f8a0: Pushed
1aaddf64804f: Mounted from srinu7358/shopfront-myapp
990c5138f5d1: Mounted from srinu7358/shopfront-myapp
5c384ea5f752: Mounted from srinu7358/shopfront-myapp
293d5db30c9f: Mounted from srinu7358/shopfront-myapp
03127cdb479b: Mounted from srinu7358/shopfront-myapp
9c742cd6c7a5: Mounted from srinu7358/shopfront-myapp
latest: digest: sha256:1104a4cb9737fc33cae8cfb60b7b0093942da0c201322e4e001ddb9fb417f23b size: 1794

build the productcatalogue micro service::
================================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue# ls

Dockerfile  pom.xml  product-catalogue.yml  src

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue# cd src/

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue/src# ls
main
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue/src# cd ..

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue# mvn clean install

[INFO] Scanning for projects...

[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  9.130 s
[INFO] Finished at: 2025-04-10T04:58:34Z
[INFO] ------------------------------------------------------------------------
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue# ls
Dockerfile  pom.xml  product-catalogue.yml  src  target


build the docker image::
=========================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue# docker image build -t productcatalogue .


[+] Building 0.6s (8/8) FINISHED                                                                                        docker:default
 => [internal] load build definition from Dockerfile                                                                              0.0s
 => => transferring dockerfile: 273B                                                                                              0.0s
 => [internal] load metadata for docker.io/library/openjdk:8-jre                                                                  0.1s
 => [internal] load .dockerignore                                                                                                 0.0s
 => => transferring context: 2B                                                                                                   0.0s
 => CACHED [1/3] FROM docker.io/library/openjdk:8-jre@sha256:667a15e7bc533a90fb39ddb7e5bed63162ac3c13a97e6c698bf4f139f51b7d33     0.0s
 => [internal] load build context                                                                                                 0.2s
 => => transferring context: 17.63MB                                                                                              0.2s
 => [2/3] ADD target/productcatalogue-0.0.1-SNAPSHOT.jar app.jar                                                                  0.1s
 => [3/3] ADD product-catalogue.yml app-config.yml                                                                                0.0s
 => exporting to image                                                                                                            0.1s
 => => exporting layers                                                                                                           0.1s
 => => writing image sha256:6c0847459aa3acde4375bfed34e3f04d029bf02a6ceedff1503657d3fc4e75e4                                      0.0s
 => => naming to docker.io/library/productcatalogue 

 verify the images::
 ==================

 root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue# docker images
 
REPOSITORY                     TAG       IMAGE ID       CREATED         SIZE
productcatalogue               latest    6c0847459aa3   9 seconds ago   291MB
stockmanager                   latest    3de0cce0b9d4   4 minutes ago   317MB
srinu7358/stockmanager-myapp   latest    3de0cce0b9d4   4 minutes ago   317MB
shopfront                      latest    3ccf19de3929   47 hours ago    320MB
srinu7358/shopfront-myapp      latest    3ccf19de3929   47 hours ago    320MB
gcr.io/k8s-minikube/kicbase    v0.0.46   e72c4cbe9b29   2 months ago    1.31GB

Tag the image:::
=====
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue# docker image tag productcatalogue 

srinu7358/productcatalogue-myapp

verify the tag image::
=====================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue# docker images

REPOSITORY                         TAG       IMAGE ID       CREATED              SIZE
productcatalogue                   latest    6c0847459aa3   About a minute ago   291MB
srinu7358/productcatalogue-myapp   latest    6c0847459aa3   About a minute ago   291MB
stockmanager                       latest    3de0cce0b9d4   5 minutes ago        317MB
srinu7358/stockmanager-myapp       latest    3de0cce0b9d4   5 minutes ago        317MB
srinu7358/shopfront-myapp          latest    3ccf19de3929   47 hours ago         320MB
shopfront                          latest    3ccf19de3929   47 hours ago         320MB
gcr.io/k8s-minikube/kicbase        v0.0.46   e72c4cbe9b29   2 months ago         1.31GB


pushed the image to docker hub::
======================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/productcatalogue# docker push srinu7358/productcatalogue-myapp

Using default tag: latest
The push refers to repository [docker.io/srinu7358/productcatalogue-myapp]
c445b4f83c8c: Pushed
24772609f9a3: Pushed
1aaddf64804f: Mounted from srinu7358/stockmanager-myapp
990c5138f5d1: Mounted from srinu7358/stockmanager-myapp
5c384ea5f752: Mounted from srinu7358/stockmanager-myapp
293d5db30c9f: Mounted from srinu7358/stockmanager-myapp
03127cdb479b: Mounted from srinu7358/stockmanager-myapp
9c742cd6c7a5: Mounted from srinu7358/stockmanager-myapp
latest: digest: sha256:5254cff2f0ce313265acee48dc8a8bd7a502ff0a6f08e3bb0dfa3ec7738676c8 size: 2001

all 3 projects images are pushed to docker hub::
==========================

![image](https://github.com/user-attachments/assets/55d1a8e2-e9ae-4a69-81dc-2b447368efa6)


edit the yaml file

root@ip-172-31-36-154:~/docker-Java-kubernetes-project# ls

README.md  kubernetes  productcatalogue  shopfront  stockmanager

root@ip-172-31-36-154:~/docker-Java-kubernetes-project# cd kubernetes/

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# ls

productcatalogue-service.yaml  shopfront-service.yaml  stockmanager-service.yaml

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# sudo vi shopfront-service.yaml

in yaml file please use your docker hub image------->srinu7358/shopfront-myapp

verify the pods,deployments,services::
=========================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get pods

No resources found in default namespace.
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get deploy

No resources found in default namespace.
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get service

NAME         TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)        AGE
kubernetes   ClusterIP   10.96.0.1        <none>        443/TCP        47h

apply the yaml file::
========

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl apply -f shopfront-service.yaml

service/shopfront created
deployment.apps/shopfront created
 above command is used to created pods,deployments,servcies

 root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po
 
NAME                         READY   STATUS    RESTARTS   AGE
shopfront-69467555f6-nzsxw   1/1     Running   0          22s

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get deploy

NAME           READY   UP-TO-DATE   AVAILABLE   AGE
shopfront      1/1     1            1           7m2s

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get service

NAME           TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
kubernetes     ClusterIP   10.96.0.1       <none>        443/TCP          2d
shopfront      NodePort    10.109.12.218   <none>        8010:32451/TCP   7m14s

we need to do other 2 micro services as well

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# sudo vi productcatalogue-service.yaml

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl apply -f productcatalogue-service.yaml

service/productcatalogue created
deployment.apps/productcatalogue created
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po

NAME                               READY   STATUS         RESTARTS     AGE
productcatalogue-968c9cbf8-dl5zx   0/1     ErrImagePull   0            15s
shopfront-69467555f6-nzsxw         1/1     Running        0            9m4s
stockmanager-6c4454c6cb-2hhfd      1/1     Running        3 (2s ago)   2m43s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get deploy

NAME               READY   UP-TO-DATE   AVAILABLE   AGE
productcatalogue   0/1     1            0           42s
shopfront          1/1     1            1           9m31s
stockmanager       1/1     1            1           3m10s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get svc

NAME               TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
kubernetes         ClusterIP   10.96.0.1        <none>        443/TCP          2d
productcatalogue   NodePort    10.105.165.177   <none>        8020:32215/TCP   56s
shopfront          NodePort    10.109.12.218    <none>        8010:32451/TCP   9m45s
stockmanager       NodePort    10.96.92.240     <none>        8030:31767/TCP   3m24s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get deploy

NAME               READY   UP-TO-DATE   AVAILABLE   AGE
productcatalogue   0/1     1            0           71s
shopfront          1/1     1            1           10m
stockmanager       1/1     1            1           3m39s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po

NAME                               READY   STATUS             RESTARTS      AGE
productcatalogue-968c9cbf8-dl5zx   0/1     ImagePullBackOff   0             77s
shopfront-69467555f6-nzsxw         1/1     Running            0             10m
stockmanager-6c4454c6cb-2hhfd      1/1     Running            4 (14s ago)   3m45s

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po

NAME                               READY   STATUS             RESTARTS      AGE
productcatalogue-968c9cbf8-dl5zx   0/1     ImagePullBackOff   0             2m8s
shopfront-69467555f6-nzsxw         1/1     Running            0             10m
stockmanager-6c4454c6cb-2hhfd      1/1     Running            5 (15s ago)   4m36s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# sudo vi productcatalogue-service.yaml

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl apply -f productcatalogue-service.yaml

service/productcatalogue unchanged
deployment.apps/productcatalogue configured
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po

NAME                                READY   STATUS             RESTARTS      AGE
productcatalogue-86c9dd7b7b-bzj29   1/1     Running            0             16s
shopfront-69467555f6-nzsxw          1/1     Running            0             14m
stockmanager-6c4454c6cb-2hhfd       0/1     CrashLoopBackOff   6 (44s ago)   8m25s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po

NAME                                READY   STATUS             RESTARTS      AGE
productcatalogue-86c9dd7b7b-bzj29   1/1     Running            0             28s
shopfront-69467555f6-nzsxw          1/1     Running            0             14m
stockmanager-6c4454c6cb-2hhfd       0/1     CrashLoopBackOff   6 (56s ago)   8m37s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl apply -f stockmanager-service.yaml

service/stockmanager unchanged
deployment.apps/stockmanager configured
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po

NAME                                READY   STATUS             RESTARTS      AGE
productcatalogue-86c9dd7b7b-bzj29   1/1     Running            0             47s
shopfront-69467555f6-nzsxw          1/1     Running            0             15m
stockmanager-6c4454c6cb-2hhfd       0/1     CrashLoopBackOff   6 (75s ago)   8m56s


if any pod is CrashLoopBackOff , please delete or update new image

delete the pod::
==================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po

NAME                                READY   STATUS             RESTARTS      AGE
productcatalogue-86c9dd7b7b-bzj29   1/1     Running            0             47s
shopfront-69467555f6-nzsxw          1/1     Running            0             15m
stockmanager-6c4454c6cb-2hhfd       0/1     CrashLoopBackOff   6 (75s ago)   8m56s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl delete po stockmanager-6c4454c6cb-2hhfd

verify the after deleted::
====================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po

NAME                                READY   STATUS    RESTARTS   AGE
productcatalogue-86c9dd7b7b-bzj29   1/1     Running   0          91s
shopfront-69467555f6-nzsxw          1/1     Running   0          16m
stockmanager-6c4454c6cb-8wkxv       1/1     Running   0          5s

all 3 micro service projects ,running pods,deploy,services::
===========================================================

root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get po

NAME                                READY   STATUS    RESTARTS      AGE
productcatalogue-86c9dd7b7b-bzj29   1/1     Running   0             2m54s
shopfront-69467555f6-wwfbv          1/1     Running   0             5s
stockmanager-6c4454c6cb-8wkxv       1/1     Running   1 (28s ago)   88s
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get deploy

NAME               READY   UP-TO-DATE   AVAILABLE   AGE
productcatalogue   1/1     1            1           10m
shopfront          1/1     1            1           19m
stockmanager       1/1     1            1           12m
root@ip-172-31-36-154:~/docker-Java-kubernetes-project/kubernetes# kubectl get svc

NAME               TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
kubernetes         ClusterIP   10.96.0.1        <none>        443/TCP          2d
productcatalogue   NodePort    10.105.165.177   <none>        8020:32215/TCP   10m
shopfront          NodePort    10.109.12.218    <none>        8010:32451/TCP   19m
stockmanager       NodePort    10.96.92.240     <none>        8030:31767/TCP   13m


>kubectl describe svc shopfront

use above command to ge the details of service 

in kubernetes we have multiple key components or objects::
======================

 YAML::

apiversion  --v1 or v2 --standadard syntax
 kind  ----deployment/service
 metadata  ----we can define name of the service
   name: shopfront
 labels ---->laben are very important in kubernetes and match with pod and matcgh with service

 spec
   type: clusterIP/NodePort

   ClusterIP::
   ==============

   ClusterIP is the default service type in Kubernetes. It creates a virtual IP (VIP) inside the cluster that other internal components (pods/services) can access — but it's not accessible from outside the cluster.

   apiVersion: v1
kind: Service
metadata:
  name: backend-service
spec:
  type: ClusterIP  # This is the default, so it can be omitted
  selector:
    app: my-backend
  ports:
    - protocol: TCP
      port: 80           # Port exposed by the service
      targetPort: 8080   # Port the container is listening on


 NodePort:
 =====
   NodePort is a type of Kubernetes Service that exposes your app outside the cluster, by opening a specific port on each worker node's IP address.

   apiVersion: v1
kind: Service
metadata:
  name: my-nodeport-service
spec:
  type: NodePort
  selector:
    app: my-app
  ports:
    - port: 80          # Service port (used internally by ClusterIP)
      targetPort: 8080  # Port on the pod
      nodePort: 30080   # Optional: if not set, Kubernetes picks one


root@k8smaster:~# kubectl get svc

NAME               TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE

kubernetes         ClusterIP   10.96.0.1        <none>        443/TCP          2d11h

nginx-app          NodePort    10.102.214.44    <none>        80:31129/TCP     2d10h

productcatalogue   NodePort    10.101.216.239   <none>        8020:32208/TCP   2d10h

shopfront          NodePort    10.102.253.116   <none>        8010:31499/TCP   2d10h

stockmanager       NodePort    10.96.66.251     <none>        8030:32579/TCP   2d10h

root@k8smaster:~# kubectl get deploy

NAME               READY   UP-TO-DATE   AVAILABLE   AGE

nginx-app          2/2     2            2           2d11h

productcatalogue   1/1     1            1           2d10h

shopfront          1/1     1            1           2d10h

stockmanager       1/6     6            1           2d10h

root@k8smaster:~# kubectl get pods

NAME                                READY   STATUS             RESTARTS          AGE

nginx-app-5777b5f95-fcx8r           1/1     Running            0                 2d11h

nginx-app-5777b5f95-v5ghx           1/1     Running            0                 2d11h

productcatalogue-869f894bc7-66f86   1/1     Running            0                 2d10h

shopfront-66555cc947-hkg9v          1/1     Running            0                 2d10h

stockmanager-7657c6dfc5-4rntl       0/1     CrashLoopBackOff   995 (4m31s ago)   2d10h

stockmanager-7657c6dfc5-4skjh       0/1     CrashLoopBackOff   1016 (112s ago)   2d10h

stockmanager-7657c6dfc5-657z6       0/1     CrashLoopBackOff   997 (2m11s ago)   2d10h

stockmanager-7657c6dfc5-7nrdc       0/1     CrashLoopBackOff   995 (3m11s ago)   2d10h

stockmanager-7657c6dfc5-f46vf       1/1     Running            996 (5m41s ago)   2d10h

stockmanager-7657c6dfc5-qznfs       0/1     CrashLoopBackOff   999 (118s ago)    2d10h


root@k8smaster:~# kubectl get svc

NAME               TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE

kubernetes         ClusterIP   10.96.0.1        <none>        443/TCP          2d11h

nginx-app          NodePort    10.102.214.44    <none>        80:31129/TCP     2d11h

productcatalogue   NodePort    10.101.216.239   <none>        8020:32208/TCP   2d10h

shopfront          NodePort    10.102.253.116   <none>        8010:31499/TCP   2d10h

stockmanager       NodePort    10.96.66.251     <none>        8030:32579/TCP   2d10h

PORTS for all 3 micro services::
=================================
shopfront                  8010:31499/TCP 

productcatalogue           8020:32208/TCP    

stockmanager               8030:32579/TCP 

Navigate to browser url shopfront with port

http://35.94.221.231:31499/

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5e7be549-ebd1-4bd5-b7e2-615f329b5a62" />

Navigate to browser url productcatalogue with port

http://35.94.221.231:32208/products

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a5dadfab-9d61-4cc4-9306-f49f910bb03b" />

Navigate to browser url stockmanager with port

http://35.94.221.231:32579/stocks

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b313bbf1-b052-4595-9426-4b1a33b8156f" />


<img width="1625" height="644" alt="image" src="https://github.com/user-attachments/assets/754f87cc-0356-4ac7-917e-597a29c1fc8c" />




21/07/2025::
===============

OpenShift Orchestration::
=============================

OpenShift Orchestration::
======================


OpenShift is an open-source container application platform built around Docker containers and Kubernetes. It's designed to help developers and IT organizations to develop, deploy, and manage applications in a highly automated environment. OpenShift offers a range of tools to make the development process more streamlined, such as CI/CD (Continuous Integration/Continuous Delivery) pipelines, a user-friendly web console, monitoring, and logging features.
Here are some key features and components of OpenShift:
1.	Kubernetes-based orchestration: OpenShift is built on top of Kubernetes, providing advanced container orchestration, scaling, and management.
2.	Developer Tools: OpenShift offers tools that make it easier for developers to deploy applications, like a simple web-based interface, CLI (Command Line Interface), and built-in support for various programming languages.
3.	Integrated CI/CD Pipelines: OpenShift integrates with Jenkins and other tools to automate the process of building, testing, and deploying applications.
4.	Security: OpenShift has several security features, including integrated authentication, network policies, and role-based access control (RBAC).
5.	Multi-cloud & Hybrid Cloud: It supports hybrid cloud environments, so applications can run across multiple infrastructures—on-premises, in the cloud, or a combination.
6.	Automated Scaling: OpenShift can automatically scale applications up or down based on resource usage.
7.	Registry and Image Management: It includes a built-in container registry to manage Docker images and store them for your applications

Red Hat Openshift Overview::
============================

- Red Hat Openshift is developed on top of Opeensource OKD ( which in turn is developed on top of opensource Kubernetes )
- supports command line interface and webconsole(GUI)
- supports Role based access control (RBAC), hence multiple users can be created with different level of access to Openshift cluster
- supports many additional features on top of all the Kubernetes features
  1. User Management
  2. Pre-integrated monitoring tools ( Prometheus & Grafana Dashboards )
  3. Out of the box - Private Container Registry
  4. Routes - a new feature only available in Openshift which is developed on top of Kubernetes Ingress
  5. Using the Kubernetes operators, the Red Hat Openshift team has many additional features on top of Kubernetes
- Openshift version upto 3 - supported many different container runtime/engines including Docker
- Openshift version 4 and above - only supports Podman Container Engine and CRI-O Container Runtime
- Due to security vulnerabilities issues in Docker, 

Using Free RedHat Developer Sandox on cloud - Openshift::
=============================

https://console.redhat.com/openshift/sandbox

we need to register free Red Hat account for  OpenShift

![image](https://github.com/user-attachments/assets/d78d4def-c589-446d-934b-3109d979b3be)

![image](https://github.com/user-attachments/assets/c4900081-a748-4f8b-b1fa-625fcccb3b5c)

Enter Redhat Login Name

![image](https://github.com/user-attachments/assets/785803bd-4d2b-480f-9d1e-9249a3d28cad)

Enter the Password

![image](https://github.com/user-attachments/assets/234e53d4-da04-4781-92d6-f44baed46307)

![image](https://github.com/user-attachments/assets/16f49b20-0632-46c7-920e-e87cd7894ce1)

click create account

![image](https://github.com/user-attachments/assets/1478f402-bb54-4166-8351-c77cb04e4303)

you will get the Email verification, please check the email

![image](https://github.com/user-attachments/assets/a0b0a9cf-d103-4fae-92d7-a70f62f8d391)

![image](https://github.com/user-attachments/assets/7182b022-e9a6-442a-96eb-a19bfd0e5401)

click the link which is you got

![image](https://github.com/user-attachments/assets/4dd9989d-3c90-4ac3-a510-ab26b2f3cf42)

Red Hat Developer Sandbox

![image](https://github.com/user-attachments/assets/42a31572-f423-4512-bfbd-5a3684b52508)

![image](https://github.com/user-attachments/assets/bfb647b7-747a-4338-b640-209587fa699f)

![image](https://github.com/user-attachments/assets/4d7d539a-9a07-4df4-9ecb-ceee0797d482)

Select Openshift Launch

![image](https://github.com/user-attachments/assets/19773259-41b0-47ae-8f76-e2386d520d1b)


click DevSandBox

![image](https://github.com/user-attachments/assets/f0218c41-9bdf-4c8b-9684-9f2c54574d63)

select Role is Developer

![image](https://github.com/user-attachments/assets/5d6e2c8f-c1d5-4ee1-a399-74ef2e03fd00)

click all selected permissions

![image](https://github.com/user-attachments/assets/17d83152-51fe-49b8-8a31-ba66884efaf1)

![image](https://github.com/user-attachments/assets/f4e855fd-a34a-4668-941b-fb4baf3c28bb)

![image](https://github.com/user-attachments/assets/2ce3c97d-de12-4e69-b2b4-6e51100d421a)

Get started

![image](https://github.com/user-attachments/assets/ac637db7-c2cc-4b8f-8841-809131f72732)

Openshift is ready and go to Developer -->Helm---->Helm charts---->search Jenkins ---Installed Jenkins Helm Charts


![image](https://github.com/user-attachments/assets/b91564a1-27d1-473c-b8b3-ce67403694fc)

Login command line::

OC ----> Openshift Client

click Copy login command at top right corner

![image](https://github.com/user-attachments/assets/4e1735af-4114-4d8d-8c01-526127c36ceb)

![image](https://github.com/user-attachments/assets/6f4cfb80-19ca-4a3b-b4be-405c6e69f812)

copy Login in with this Token

![image](https://github.com/user-attachments/assets/11a7edbb-f3aa-4e79-8457-90dedfb0af06)

![image](https://github.com/user-attachments/assets/3d18ae45-f2d6-43ca-b8e5-95d5b2d23a64)

Getting oc command is not found

So we need to download the oc from google

1 download oc.exe https://developers.redhat.com/openshift/command-line-tools
2 navigate to environment variables -> system variables -> new
3 add here: /path/to/the/oc.exe

https://docs.redhat.com/en/documentation/openshift_container_platform/4.8/html/cli_tools/openshift-cli-oc#cli-installing-cli_cli-developer-commands

https://access.redhat.com/downloads/content/290/ver=4.18/rhel---9/4.18.7/x86_64/product-software

OC download LInk::
=====================

OC
is a client tool used to create and manage Openshift resources in OpenShift
it makes REST call to API Server

https://access.redhat.com/downloads/content/290/ver=4.18/rhel---9/4.18.8/x86_64/product-software

Download Windows client

![image](https://github.com/user-attachments/assets/14d36459-8cf3-4ba1-8cb5-361f34730aa0)

Download the oc for window and extracted all the files

![image](https://github.com/user-attachments/assets/85d30663-3fc1-4a7a-878a-3f316b74ce7c)

Open from command line

![image](https://github.com/user-attachments/assets/999801e8-1078-474c-9ab1-27e4bb3e8a21)


![image](https://github.com/user-attachments/assets/3122d471-9a89-467c-b986-d9229f95db9f)

Switch project
>oc project <projectname>
>oc project srinu942-dev

![image](https://github.com/user-attachments/assets/31f81eac-41a4-403b-8de3-3edf5089e4f0)

OpenShift resources
•	Deployment (K8s resource)
•	ReplicaSet (K8s resource)
•	Pod (K8s resource)
•	Job (K8s resource)
•	DaemonSet (K8s resource)
•	StatefulSet (K8s resource)
•	Build ( OpenShift resource - Custom Resource added by OpenShift )
•	ImageStream ( OpenShift resource - Custom Resource added by OpenShift )
•	DeploymentConfig ( OpenShift resource - Custom Resource added by OpenShift )

Deployment command looks like this
>oc create deployment nginx --image=bitnami/nginx:latest --replicas=3

![image](https://github.com/user-attachments/assets/dbc5a3bd-aa15-4346-b753-9621d8dd3e81)

Deployment::
=================
This is a JSON/YAML definition which is stored in etcd database
The deployment is managed by Deployment Controller
when we applications, they are deployed as Deployment with Kubernetes/OpenShift
Deployment Controller creates ReplicaSet, which is then managed by ReplicaSet Controller
Deployment has one or more ReplicaSet(s)

ReplicaSet::
=============
This is a JSON/YAML definition which is stored in etcd database
The ReplicaSet is managed by ReplicaSet Controller
ReplicaSet capture details like
How many Pod instances are desired?
ReplicaSet Controller reads the ReplicaSet definition and learns the desired Pod instance count
ReplicaSet Controller creates so many Pod definition as indicated in the ReplicaSet
ReplicaSet Controller ensures the desired Pod count matches with the actual Pod count, whenever a Pod crashes, it is the responsibility of ReplicaSet Controller to ensure the desired and actual Pods are equal
ReplicaSet has one or more Pods

Pod::
====
is a collection of one or more Containers
IP address is assigned on the Pod level not on the Container level
If two containers are in the same Pod, there will be sharing IP Address of the Pod
within container, application are deployment ( tomcat,mysql, nginx these are applications )
recommended best practice,only one application should be there in a Pod
Pods are scheduled by Scheduler onto some Node
every Pod has a Network Stack and Network Interface Card (NIC)

Kubelet::
===========
is a daemon service that interacts with the Container Runtime on the current node/server where kubelet is running
kubelet downloads the required container image and creates the Pod containers
kubelet frequently reports the status of Pod container status to the API server
kubelet also monitors the health of POds running on the node and ensures they are healthy
kubelet will there on every node ( master and worker nodes )

kube-proxy::
=============
is a Pod that runs one instance per node (both master and worker nodes)
provides load-balancing a group of similar Pods
Sample Demo Project fro Openshift

Kubectl::
========
is a client tool used to create and manage deployments and services in Kubernetes
it also works in OpenShift
it make REST call to API Server

OC::
===
is a client tool used to create and manage Openshift resources in OpenShift
it makes REST call to API Server

https://github.com/wicksy/openshift-demo-app/tree/master
https://github.com/wicksy/openshift-demo-app

Login command line::

OC ----> Openshift Client

click Copy login command at top right corner

![image](https://github.com/user-attachments/assets/4e1735af-4114-4d8d-8c01-526127c36ceb)

![image](https://github.com/user-attachments/assets/6f4cfb80-19ca-4a3b-b4be-405c6e69f812)

copy Login in with this Token

![image](https://github.com/user-attachments/assets/11a7edbb-f3aa-4e79-8457-90dedfb0af06)

![image](https://github.com/user-attachments/assets/3d18ae45-f2d6-43ca-b8e5-95d5b2d23a64)

Getting oc command is not found

So we need to download the oc from google

1 download oc.exe https://developers.redhat.com/openshift/command-line-tools
2 navigate to environment variables -> system variables -> new
3 add here: /path/to/the/oc.exe

https://docs.redhat.com/en/documentation/openshift_container_platform/4.8/html/cli_tools/openshift-cli-oc#cli-installing-cli_cli-developer-commands

https://access.redhat.com/downloads/content/290/ver=4.18/rhel---9/4.18.7/x86_64/product-software

OC download LInk::
=====================

OC
is a client tool used to create and manage Openshift resources in OpenShift
it makes REST call to API Server

https://access.redhat.com/downloads/content/290/ver=4.18/rhel---9/4.18.8/x86_64/product-software

Download Windows client

![image](https://github.com/user-attachments/assets/14d36459-8cf3-4ba1-8cb5-361f34730aa0)

Download the oc for window and extracted all the files

![image](https://github.com/user-attachments/assets/85d30663-3fc1-4a7a-878a-3f316b74ce7c)


OC (Openshift Client) Environment Path Setup::
=================================================

Go to Environment Variable

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/49b284e4-d6f4-4174-882b-eba40f7278a7" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/785ec522-2004-4b35-a508-ae66bb170e3a" />

Set the User Variables::
===========================

C:\Openshift\oc\


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c5c9a09a-bd7a-445e-ac0a-5ae719ee5b7b" />

Set the System Variables and Path::
===================================

C:\Openshift\oc\

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fb77f2ad-5bd6-4e30-9e1f-88c40f65d4a5" />

click OK ----> OK----> OK

Go to command prompt

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/49ebb7c8-f469-4046-9c44-2030129aa615" />

verify the OC

>oc


verify the oc verison

>oc version


C:\Users\HP>oc version

Client Version: 4.19.3

Kustomize Version: v5.5.0

Server Version: 4.18.16

Kubernetes Version: v1.31.8


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/48fd2ee7-1510-416d-8124-ec3ac161fec5" />


Clone the Project from Openshift Command line(cli)::
========================================================

>git clone https://github.com/srinfotech7358/docker-Java-kubernetes-project.git


C:\Users\HP>git clone https://github.com/srinfotech7358/docker-Java-kubernetes-project.git

Cloning into 'docker-Java-kubernetes-project'...

remote: Enumerating objects: 173, done.

remote: Counting objects: 100% (58/58), done.

remote: Compressing objects: 100% (47/47), done.

Rremote: Total 173 (delta 33), reused 10 (delta 10), pack-reused 115 (from 1)

Receiving objects: 100% (173/173), 31.47 KiB | 4.00 KiB/s, done.

Resolving deltas: 100% (41/41), done.


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2eb89ce1-14e2-4cff-92de-2aa757f9a2cd" />

>cd docker-Java-kubernetes-project

>cd kubernetes

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fb1c3b1f-4da1-4cff-9f5a-4f72e0aae4ce" />

>oc projects

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/250aba7f-14e3-46b7-8f1c-032da5197b11" />

switch the project

>oc project <projectname OR Namespace>

>oc project srinfotech7358-dev

C:\Users\HP\docker-Java-kubernetes-project\kubernetes>oc project srinfotech7358-dev

Already on project "srinfotech7358-dev" on server "https://api.rm1.0a51.p1.openshiftapps.com:6443".

C:\Users\HP\docker-Java-kubernetes-project\kubernetes>


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/198007de-0f67-4ba8-9d33-33ae5386f1d7" />


create the openshift deployment::
====================================

Syntax::
========

>kubectl apply -f <playbook/yaml/yml>

>oc apply -f shopfront-service.yaml

>oc apply -f productcatalogue-service.yaml

>oc apply -f stockmanager-service.yaml

all 3 Micro services Deployemnts is created

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6ec769fc-fed2-4601-92fd-7ac0a0ad7f13" />


expose Openshift Services::
============================

Syntax::
===============

>oc expose service <servicename>

>oc expose deployment <deploymentName>

>oc get svc OR services

C:\Users\HP\docker-Java-kubernetes-project\kubernetes>oc get svc
NAME                          TYPE           CLUSTER-IP       EXTERNAL-IP                                                  PORT(S)                                              AGE
example                       ClusterIP      172.30.120.21    <none>                                                       80/TCP                                               7d6h
jenkins                       ClusterIP      172.30.2.244     <none>                                                       80/TCP                                               7d7h
jenkins-jnlp                  ClusterIP      172.30.35.46     <none>                                                       50000/TCP                                            7d7h
modelmesh-serving             ClusterIP      None             <none>                                                       8033/TCP,8008/TCP,8443/TCP,2112/TCP                  7d7h
my-app-service                ClusterIP      172.30.167.153   <none>                                                       8080/TCP                                             9h
nginx                         ClusterIP      172.30.43.7      <none>                                                       8080/TCP                                             7h30m
petclinic-00001               ClusterIP      172.30.121.230   <none>                                                       80/TCP,443/TCP                                       7h41m
petclinic-00001-private       ClusterIP      172.30.127.53    <none>                                                       80/TCP,443/TCP,9090/TCP,9091/TCP,8022/TCP,8012/TCP   7h41m
productcatalogue              NodePort       172.30.36.130    <none>                                                       8020:30170/TCP                                       8h
shopfront                     NodePort       172.30.246.166   <none>                                                       8010:31109/TCP                                       8h
sonarqube                     ClusterIP      172.30.197.221   <none>                                                       9000/TCP                                             7h13m
spring-ms-git                 ExternalName   <none>           kourier-internal.knative-serving-ingress.svc.cluster.local   80/TCP                                               7d6h
spring-ms-git-00001           ClusterIP      172.30.134.127   <none>                                                       80/TCP,443/TCP                                       7d6h
spring-ms-git-00001-private   ClusterIP      172.30.131.234   <none>                                                       80/TCP,443/TCP,9090/TCP,9091/TCP,8022/TCP,8012/TCP   7d6h
stockmanager                  NodePort       172.30.158.37    <none>                                                       8030:31782/TCP                                       7h53m


>oc expose service shopfront

>oc expose service productcatalogue

>oc expose service stockmanager

all 3 micro services are up & running in Openshift cluster

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/494b1042-e10b-424a-a50b-0b632e021a9e" />


Shopfront::
=============

http://shopfront-srinfotech7358-dev.apps.rm1.0a51.p1.openshiftapps.com/

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b73a85c7-d73e-4f25-bd98-364afab07df5" />


productcatalogue::
====================

http://shopfront-srinfotech7358-dev.apps.rm1.0a51.p1.openshiftapps.com/products

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a105b423-c20b-4823-8ae4-eb8ca69944a5" />


stockmanager::
===================

http://stockmanager-srinfotech7358-dev.apps.rm1.0a51.p1.openshiftapps.com/stocks

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/393c4678-fd19-49ed-8def-bc08b7190529" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5f4eed44-9f10-4549-84bb-6506d65911fa" />


Deploy Nginx Application To Openshift Platform::CLI
=====================================================

>oc create deployment nginx --image=bitnami/nginx:latest

>oc expose deployment nginx --port=8080 --target-port=8080 --name=nginx


http://route-unfortunate-smelt-srinfotech7358-dev.apps.rm1.0a51.p1.openshiftapps.com/


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7b164789-3b24-4212-8d53-989011144a96" />


Deploy Spring-ms Application To Openshift Platform::Manually
=========================================================

https://github.com/srinfotech7358/spring-ms.git

Go to Openshift Developer page

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/91a57b60-4e62-4166-92bf-b86266427b69" />

Click Add

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d48386bd-9f19-4765-b783-a1e310af59b2" />


Git Repository

Import From Git

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c8b803b5-6203-43ef-b2f1-fcdf195c5e8a" />


Copy Git Repo URL * From Github 


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/989f5013-211c-46dd-990f-210b4e9ea51a" />


Click Create

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1db49867-ed7f-44eb-9632-a117b3c48d2f" />


github project url for spring-ms

https://github.com/srinfotech7358/spring-ms.git

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/55c5a788-80a8-4ba0-9853-3fd7b0a2960c" />


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/250e2cfb-ccfb-4b68-8f76-b3fab4f514d2" />


https://spring-ms-git-srinfotech7358-dev.apps.rm1.0a51.p1.openshiftapps.com/

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/008c0718-ec49-4ddf-bb50-1bbcf82557fa" />


C:\Users\HP\docker-Java-kubernetes-project\kubernetes>oc get svc
NAME                          TYPE           CLUSTER-IP       EXTERNAL-IP                                                  PORT(S)                                              AGE
example                       ClusterIP      172.30.120.21    <none>                                                       80/TCP                                               7d6h
jenkins                       ClusterIP      172.30.2.244     <none>                                                       80/TCP                                               7d7h
jenkins-jnlp                  ClusterIP      172.30.35.46     <none>                                                       50000/TCP                                            7d7h
modelmesh-serving             ClusterIP      None             <none>                                                       8033/TCP,8008/TCP,8443/TCP,2112/TCP                  7d7h
my-app-service                ClusterIP      172.30.167.153   <none>                                                       8080/TCP                                             9h
nginx                         ClusterIP      172.30.43.7      <none>                                                       8080/TCP                                             7h30m
petclinic-00001               ClusterIP      172.30.121.230   <none>                                                       80/TCP,443/TCP                                       7h41m
petclinic-00001-private       ClusterIP      172.30.127.53    <none>                                                       80/TCP,443/TCP,9090/TCP,9091/TCP,8022/TCP,8012/TCP   7h41m
productcatalogue              NodePort       172.30.36.130    <none>                                                       8020:30170/TCP                                       8h
shopfront                     NodePort       172.30.246.166   <none>                                                       8010:31109/TCP                                       8h
sonarqube                     ClusterIP      172.30.197.221   <none>                                                       9000/TCP                                             7h13m
spring-ms-git                 ExternalName   <none>           kourier-internal.knative-serving-ingress.svc.cluster.local   80/TCP                                               7d6h
spring-ms-git-00001           ClusterIP      172.30.134.127   <none>                                                       80/TCP,443/TCP                                       7d6h
spring-ms-git-00001-private   ClusterIP      172.30.131.234   <none>                                                       80/TCP,443/TCP,9090/TCP,9091/TCP,8022/TCP,8012/TCP   7d6h
stockmanager                  NodePort       172.30.158.37    <none>                                                       8030:31782/TCP                                       7h53m


![Uploading image.png…]()





22/07/2025::
============

Splunk::
============

Splunk is a powerful platform for searching, monitoring, and analyzing machine-generated big data via a web-style interface. It’s widely used for:

1.Log aggregation

2.Monitoring and observability

3.Security (SIEM/SOAR)

4.Dashboards and alerting

Splunk Integrate With Jenkins::
===========================

Jenkins install link

https://www.cherryservers.com/blog/install-jenkins-ubuntu

Splunk install link

https://www.splunk.com/en_us/download/splunk-enterprise.html

Create Account

![image](https://github.com/user-attachments/assets/4275dc32-37e7-41a4-8634-89bff7f6ce38)

Click Create your account


Verify the email

![image](https://github.com/user-attachments/assets/65095d9c-4f93-4d44-9f0c-50d11c752093)

![image](https://github.com/user-attachments/assets/9479e5ef-2f2f-481a-9ff2-796971238eb7)

Copy Wget URL

wget -O splunk-9.4.1-e3bdab203ac8-linux-amd64.deb https://download.splunk.com/products/splunk/releases/9.4.1/linux/splunk-9.4.1-e3bdab203ac8-linux-amd64.deb

![image](https://github.com/user-attachments/assets/91dcd374-23b5-4951-ba91-2031f3df5e7a)

Create one AWS Ubuntu Machine and past the Wget url and enter

![image](https://github.com/user-attachments/assets/da0d2f58-6893-41a3-87dc-9cfde5abdb54)

![image](https://github.com/user-attachments/assets/6ca6e5cc-e93e-4fc2-ad07-321d2b546b6d)

Download successfully using that wget url

![image](https://github.com/user-attachments/assets/9ab0f410-654b-41bf-aeaf-0ddd9cb8f9bf)

Go to splunk tutorial
https://docs.splunk.com/Documentation/Splunk/9.4.1/SearchTutorial/WelcometotheSearchTutorial

go to below link

https://docs.splunk.com/Documentation

click Splunk enterprise
![image](https://github.com/user-attachments/assets/e29a16ac-e8c0-4001-b9e7-0a38083a143c)

Search tutorial
![image](https://github.com/user-attachments/assets/a4c67579-d4a8-433f-b5f8-b7e8c03a6440)

Part 1: Getting started

•	Install Splunk Enterprise

![image](https://github.com/user-attachments/assets/8cd7631b-f021-4e17-8c17-c745719cd89e)

Install the Splunk Enterprise DEB package
![image](https://github.com/user-attachments/assets/9d25b1f5-610b-424c-a382-ada36c84def9)

dpkg -i splunk_package_name.deb.

>sudo dpkg -i

![image](https://github.com/user-attachments/assets/eab015f9-658c-40a4-a0a9-f3d4a5fe9c2e)

Run below command in ubuntu

>sudo dpkg -i splunk-9.4.1-e3bdab203ac8-linux-amd64.deb

![image](https://github.com/user-attachments/assets/b927efe6-7bf2-47f1-bc5c-08362cd95812)


![image](https://github.com/user-attachments/assets/a071e14d-4dda-415c-8bdb-ed610ce66b56)

To start the splunk please run below command

>sudo /opt/splunk/bin/splunk enable boot-start


![image](https://github.com/user-attachments/assets/322f83e9-90a3-4e9e-b4d4-09e08d19ff7f)


Click enter

![image](https://github.com/user-attachments/assets/b932045c-f586-439d-9c13-f2afd9035922)


![image](https://github.com/user-attachments/assets/790d67c5-cc65-4a8a-a2ed-1f52f878cfea)


![image](https://github.com/user-attachments/assets/d65bda8a-2255-4231-9d9b-e2914798a31f)


Username:: 

![image](https://github.com/user-attachments/assets/a1a5f381-3ded-4291-b779-561b2373e4e1)


Password:

![image](https://github.com/user-attachments/assets/a95d259e-b0b6-4299-98e4-c690b057bbf5)


![image](https://github.com/user-attachments/assets/2ffcc310-04f3-4e41-b09d-63087230510d)


For enabled boost start right for that we need to run below command

>sudo ufw allow openSSH

![image](https://github.com/user-attachments/assets/857857f0-9262-4d83-af93-53097331bfcd)


![image](https://github.com/user-attachments/assets/cc881e9c-94c1-454f-a8cc-4a375778c1e8)


openSSH means open por 22

enabled port for splunk

>sudo ufw allow 8000


![image](https://github.com/user-attachments/assets/0112d03f-4f19-43cc-b27a-0b5d5248fa4c)


Check the splunk status
>sudo ufw status

Inactive, so we need to enabled


![image](https://github.com/user-attachments/assets/ab0950ca-af19-439f-bf79-401d208c175d)


Enabled splunk

>sudo ufw enable


![image](https://github.com/user-attachments/assets/4740cb2b-3ff0-4f2f-a1c9-af5e2bd8af6b)


![image](https://github.com/user-attachments/assets/f8ef0cda-91bb-499f-be3b-257c106657f2)


Now see openSSH port -22 allowed
8000 port enabled allowed 

Now we need to start splunk
>sudo /opt/splunk/bin/splunk start


![image](https://github.com/user-attachments/assets/d0593020-69ba-4212-9046-ff69e665593f)


![image](https://github.com/user-attachments/assets/37cf9f5e-85b2-442b-9e28-3dcac692605e)


Enter user/pwd
Srinu/Srinu@7358

![image](https://github.com/user-attachments/assets/e0313ff9-9ddc-42e6-9e46-6152e40c0a51)


![image](https://github.com/user-attachments/assets/12a6cc79-6efa-42eb-a0ea-70d1084d84da)


Go Apps----- Find More Apps

![image](https://github.com/user-attachments/assets/e0123b5d-c8eb-42d8-9eff-099b55046509)


Splunk App for Jenkins  ----we need to install this app in splunk to integrate with Jenkins

![image](https://github.com/user-attachments/assets/00be0b2e-ba7c-4660-aa40-4ae7e54b8e87)


Click install
Asking UN/PWD

NOTE:: make sure you should provide the UN/PWD is splunk enterprise at the time of create the splunk account right

![image](https://github.com/user-attachments/assets/91c02e5a-9b89-4cdd-8807-34084482a48e)

Click agree & install

![image](https://github.com/user-attachments/assets/fdaaaa1b-a921-40a1-a1d4-195e62da4cc1)


![image](https://github.com/user-attachments/assets/ff25f0de-c433-42ae-b6dd-47de03da9a22)


![image](https://github.com/user-attachments/assets/9664e7c6-53af-42f2-ada4-4c4d893d128e)


Click splunk enterprise

We can see splunk for Jenkins


![image](https://github.com/user-attachments/assets/690e9a3f-b577-4f7d-86fc-3c5585d0cc22)


Go to settings

![image](https://github.com/user-attachments/assets/ebc01f35-ef98-40a6-ae30-ceb03d7a7e79)


Click data inputs

![image](https://github.com/user-attachments/assets/70250ace-d56a-4429-af88-7773f67919c5)


![image](https://github.com/user-attachments/assets/f97f0d52-0141-4b1c-bb27-08bf8ccc414b)


Click HTTP Event Collector

![image](https://github.com/user-attachments/assets/9250ef52-d8d2-4591-b0ad-4df3b387053b)


Click Global settings

![image](https://github.com/user-attachments/assets/5be60128-7a12-4ea7-bb97-fe0915dd95c7)


Uncheck

Enable SSL


![image](https://github.com/user-attachments/assets/97643fac-bde5-42fc-952b-9dda35662bfe)


For integrate with Jenkins we required New token

Click New Token


![image](https://github.com/user-attachments/assets/8af2c367-bd84-4f37-af82-b6f2ef917912)


Provided name

![image](https://github.com/user-attachments/assets/e900004d-8aa3-426c-b44a-8f86fd472a13)


Next

![image](https://github.com/user-attachments/assets/c16959b5-c0cf-4fa9-81b0-d13e5abf8223)


Click submit

![image](https://github.com/user-attachments/assets/b045b901-267b-430f-86ba-3fa9e9d5b626)


Click start searching

![image](https://github.com/user-attachments/assets/3a51da53-920b-4057-8fde-9183fa0a71b7)


Go to setting - Data Inputs –

Get the token value

![image](https://github.com/user-attachments/assets/4b03dc1a-5c78-4796-9865-57c765b7be9f)


To integrate with Jenkins, we need to install Splunk plugin in Jenkins

![image](https://github.com/user-attachments/assets/555c1b5c-ba85-4bae-b97e-5ba90118851b)


Go to System
Splunk for Jenkins Configuration


![image](https://github.com/user-attachments/assets/72e57b42-64ab-4c2a-9d9b-19bd8dfa8387)


![image](https://github.com/user-attachments/assets/3f1e30e1-f3a8-48fc-b818-1bb5c6a9db68)



