# Git training

Tasks
===

Questions from https://www.edureka.co/blog/interview-questions/git-interview-questions/


**1. What is the difference between Git and SVN?**

|           Git             |               SVN              |
|---------------------------|--------------------------------|
|Git has a Distributed Model.|SVN has a Centralized Model.|
|In git we create only .git directory.|In SVN we create .svn directory in each folder.|
|In git every user has their own copy of code on their local like their own branch.|In SVN there is central repository has working copy that also make changes and committed in central repository.|
|Push/pull operations are faster|Push/pull operations are slower|

====

**2. What is Git?**

Git is a smart distributed version control system. Git has a remote repository which is stored in a server and a local repository which is stored in the computer of each developer. This means that the code is not just stored in a central server, but the full copy of the code is present in all the developers’ computers. 

===

**3. What is a distributed VCS?**

Every contributor can get a local copy of the main repository and add code in parallel. With an operation "pull” developers can update their local repositories with new data. Also this operation affects to the main repository from their local repository.

===

**4. What is the difference between Git and Github?**

|           Git             |           Github          |
|---------------------------|---------------------------|
|Git is a software          |GitHub is a service        |
|Git is a command-line tool |GitHub is a graphical user interface|
|Git is installed locally on the system|GitHub is hosted on the web|

===

**5. What are the benefits of using Version Control System?**

First, there is a complete long-term history of changes for each file. Every change made by many developers over the years.  Changes include creating and deleting files, editing their content, author, date, number of the ticket/branch and commits about the purpose of each change.

Branching and merging. Concurrently work of all team members. Bringing workflows together allows developers to verify that changes in each branch do not conflict.

===
**6. What language is used in Git?**

Git is written in C. Almost 50% of Git's code is written in C. 

===

**7. Mention the various Git repository hosting functions.**

Github
Gitlab
Bitbucket
SourceForge
GitEnterprise

===

**8. What is a commit message?**

``` git commit ```
It will launch a text editor prompting us for a commit message.
``` git commit -a ```
The ```-a``` flag is used to tell git to commit the new contents of all tracked files that have changed.

===

**9. How can you fix a broken commit?**

The ```--amend``` flag is a convenient way to fix the error made in the commit log message. This command allows you to edit the message of the previous commit without changing its snapshot.

===

**10. What is a repository in Git?**

Repository in Git is a place where Git stores all the files. Git can store the files either on the local repository or on the remote repository.
 
