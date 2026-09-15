# OJF - Oracle Java Foundations (Oracle University)

Ready to kick off your Java programming journey? In this course, you’ll dive into the essentials—variables, loops, arrays, classes, objects, and decision structures—while getting a solid grip on object-oriented programming. You'll build real code as you go, with hands-on practice to turn theory into working Java programs. It’s the perfect starting point if you want to understand how Java works and start creating your own applications.

**Course**: [https://mylearn.oracle.com/ou/course/oracle-java-foundations/152254/251448](https://mylearn.oracle.com/ou/course/oracle-java-foundations/152254/251448)

## Course content

- [x] 01 - Overview

  - [x] 01 - Course Introduction

## Repository configuration

Each submodule in this repository contains the code examples of the original course.

### Create new submodules

Create a new repository on Github, then execute the following commands to link the new repository as a submodule of the main repository:

```
$ cd oracle-java-foundations
$ git submodule add -b main git@github.com:ensomugnog/ojf-submodule
```

Using the **-b** argument means we want to follow the main branch of the new repository, and after running this command we’ll have a new directory named `ojf-submodule/`, this directory will automaticaly checkout the main branch for you to be ready to make changes.

### Update main repository with latest submodule changes

First make sure the submodule changes have been commited and pushed to the orign repository, then run the following commands:

```
$ git status
$ git stage .
$ git commit -m 'ojf-submodule'
$ git push
```

### Clone Repository with submodules

If you want to clone a repository including its submodules you can use the --recursive parameter, use the --jobs parameter to fetch multiple submodules at the same time, download up to 8 submodules at once use --jobs 8

```
$ git clone --recursive --jobs 8 git@github.com:ensomugnog/oracle-java-foundations.git
```

### Delete a submodule from a repository

Currently Git provides no standard interface to delete a submodule. To remove a submodule `ojf-submodule` you need to:

```
$ git submodule deinit -f ojf-submodule
$ rm -rf .git/modules/ojf-submodule
$ git rm -f ojf-submodule
```

### Checkout a commit

To checkout a Git commit, you will need the commit hash.

```
$ git checkout 4aa03973d004286558465a8d86bcccfdc7b46505
$ git reset --hard
$ git checkout main
```