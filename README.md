# OJF - Oracle Java Foundations (Oracle University)

Ready to kick off your Java programming journey? In this course, you’ll dive into the essentials—variables, loops, arrays, classes, objects, and decision structures—while getting a solid grip on object-oriented programming. You'll build real code as you go, with hands-on practice to turn theory into working Java programs. It’s the perfect starting point if you want to understand how Java works and start creating your own applications.

**Course**: [https://mylearn.oracle.com/ou/course/oracle-java-foundations/152254/251448](https://mylearn.oracle.com/ou/course/oracle-java-foundations/152254/251448)

## Course Progress: 37.5%

## Course content

- [x] 01 - Overview

  - [x] 01 - Course Introduction

- [x] 02 - Introduction to Java Basics
  
  - [x] 01 - Introduction to Java

  - [x] 02 - A Simple Java Application
  
  - [x] 03 - Java Development Tools
  
  - [x] 04 - Practice 1-1: Course Environment Setup [ [ojf-practice-01](https://github.com/ensomugnog/ojf-practice-01) -> [9518591](https://github.com/ensomugnog/ojf-practice-01/commit/95185914543a65d824717fa3605b3d0d6473222f) ]
  
  - [x] 05 - Practice 1-2: Creating, Compiling, and Executing a Java Application [ [ojf-duke-labs](https://github.com/ensomugnog/ojf-duke-labs) -> [cdc658d](https://github.com/ensomugnog/ojf-duke-labs/commit/8fb4b72a5a350dc573dbebb7a17e093115809901) ]
  
- [x] 03 - Handling Text and Numbers
  
  - [x] 01 - Variables, Constants and Types
  
  - [x] 02 - Operators
  
  - [x] 03 - Operation Results 
  
  - [x] 04 - Practice 2-1: Working with Variables and Constants [ [ojf-practice-02](https://github.com/ensomugnog/ojf-practice-02) -> [8fb4b72](https://github.com/ensomugnog/ojf-practice-02/commit/8fb4b72a5a350dc573dbebb7a17e093115809901) ]
  
  - [x] 05 - Work with Text values
  
  - [x] 06 - Practice 3-1: Working with Strings [ [ojf-practice-03](https://github.com/ensomugnog/ojf-practice-03) -> [694e224](https://github.com/ensomugnog/ojf-practice-03/commit/694e224167eddeb14f58cb26b9447b5609fcdb74) ]

- [x] 04 - Arrays, Conditions, and Loops

  - [x] 01 - Work with Arrays
  
  - [x] 02 - Practice 4-1: Working with Arrays [ [ojf-practice-04](https://github.com/ensomugnog/ojf-practice-04) -> [9b4b5bd](https://github.com/ensomugnog/ojf-practice-04/commit/9b4b5bd37f47cd34df7fac3f6ac8a81e09052f3f) ]
  
  - [x] 03 - Write Loops

  - [x] 04 - Write if/else constructs
  
  - [x] 05 - Write switch/case constructs
  
  - [x] 06 - Practice 5-1: Controlling Program Flow [ [ojf-practice-05](https://github.com/ensomugnog/ojf-practice-05) -> [4e8ad06](https://github.com/ensomugnog/ojf-practice-05/commit/4e8ad066ae58e400a4c14d25392f4c3bc2ce0a43) ]

- [x] 05 - Defining Classes and Creating Objects

  - [x] 01 - Write Methods
  
  - [x] 02 - Practice 6-1: Working with Methods [ [ojf-practice-06](https://github.com/ensomugnog/ojf-practice-06) -> [1a351bb](https://github.com/ensomugnog/ojf-practice-06/commit/1a351bb57fb2b058a016b0817fd14cb57d56609d) ]
  
  - [x] 03 - Create Classes and Objects
  
  - [x] 04 - Work with Objects
  
  - [x] 05 - Overload Methods
  
  - [x] 06 - Practice 7-1: Working with Classes [ [ojf-duke-labs](https://github.com/ensomugnog/ojf-duke-labs) -> [6a79b9d](https://github.com/ensomugnog/ojf-duke-labs/commit/6a79b9dd43fee5aa7444ec7644baf963dea3e276) ]

## Repository configuration

Each submodule in this repository contains the code examples of the original course.

### Create new submodules

Create a new repository on Github, then execute the following commands to link the new repository as a submodule of the main repository:

```
$ cd oracle-java-foundations
$ git submodule add -b main git@github.com:ensomugnog/ojf-practice-06
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