# CSE15L Lab Report 4 Researching Commands
Siddharth Gaywala
CSE15L

***

## Step 1: Delete any existing forks of the repository you have on your account
I typed the following command when already logged into the ieng6 server (see step 4). Make sure you are in the parent directory of lab7/.
```
$ rm -rf lab7/
```

## Step 2: Fork the repository
I did this on github.

## Step 3: Start the Timer
Start the timer on your phone or other device! :)
![image](https://user-images.githubusercontent.com/122569404/221037619-447fe4a5-d4fd-44d5-b7ac-fc8f77add389.png)
Source for image: https://i.ebayimg.com/images/g/n3kAAOSw8vNaVtID/s-l640.jpg


## Step 4: Log into ieng6
I type the following command to log into ieng6:
```
$ ssh cs15lwi23arm@ieng6.ucsd.edu
```
I don't need to enter my password, since I did the libgen rsa key.
![image](https://user-images.githubusercontent.com/122569404/221037846-61b75bd6-01cd-4603-a78a-c250db284922.png)



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
$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```

## Step 7: Edit the code file to fix the failing test
To edit the code, I typed the following command:  
```
$ nano ListExamples.java
```
Then, after doing nano, I held the down key until I reached Line 43, where I changed Line43 from "index1 += 1;" to "index2 += 1;"
Then, I did <ctrl O> and then <enter> and then <ctrl X>.

## Step 8: Run the tests, demonstrating that they now succeed
```
$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```

## Step 9: Commit and push the resulting change to your Github account
```
$ git add ListExamples.java
$ git commit -m "Fixed ListExamples.java"
$ git push origin main
```
