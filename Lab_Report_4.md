# CSE15L Lab Report 4 Researching Commands
Siddharth Gaywala
CSE15L

***

## Step 4: Log into ieng6
I type the following command to log into ieng6:
```
$ ssh cs15lwi23arm@ieng6.ucsd.edu
```
I don't need to enter my password, since I did the libgen rsa key.

## Step 5: Clone your fork of the repository from your Github account
To clone the fork, I typed the following command:
```
$ git clone git@github.com:sgaywalaUCSD/lab7.git
```

where git@github.com:sgaywalaUCSD/lab7.git is my ssh link to my lab7 fork.

## Step 6: Run the tests, demonstrating that they fail
To run the tests, I typed the following command:
```
$ cd lab7
$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests.java
```

## Step 7: Edit the code file to fix the failing test

## Step 8: Run the tests, demonstrating that they now succeed

## Step 9: Commit and push the resulting change to your Github account
