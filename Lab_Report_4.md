# CSE15L Lab Report 4 Researching Commands
Siddharth Gaywala
CSE15L

***

## Step 1: Delete any existing forks of the repository you have on your account
I typed the following command when already logged into the ieng6 server (see step 4). Make sure you are in the parent directory of lab7/.
```
$ rm -rf lab7/
```
![image](https://user-images.githubusercontent.com/122569404/221385766-8f95800a-e5f1-4820-b86e-98501b2fc3f0.png)


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

The 3 letter code (mine was arm) will vary based on the student.

## Step 5: Clone your fork of the repository from your Github account
To clone the fork, I typed the following command:
```
$ git clone git@github.com:sgaywalaUCSD/lab7.git
```

where `git@github.com:sgaywalaUCSD/lab7.git` is my ssh link to my lab7 fork.
![image](https://user-images.githubusercontent.com/122569404/221385329-ce4318be-57d5-41be-ae15-9cc80fff51fd.png)


## Step 6: Run the tests, demonstrating that they fail
To run the tests, I typed the following command:
```
$ cd l<tab><enter> //should autocomplete to lab7/ assuming no other paths start with l
$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
$ java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore L<tab>T<tab><backspace><enter> //should become ListExamplesTests
```
![image](https://user-images.githubusercontent.com/122569404/221385381-5a0ee141-d6d0-4b00-b712-2ecf87943948.png)


## Step 7: Edit the code file to fix the failing test
To edit the code, I typed the following command:  
```
$ nano L<tab>.j<tab><enter> //should become ListExamples.java
```
![image](https://user-images.githubusercontent.com/122569404/221385455-1d7f76c4-3322-4b90-85e8-2d007cafdfa2.png)

Then, after doing nano, I held the down key until I reached Line 43, where I changed Line43 from "index1 += 1;" to "index2 += 1;" (moving the cursor using the right key and backspace and then typing 2)
![image](https://user-images.githubusercontent.com/122569404/221385486-df1da99a-1bcf-4646-8135-47c5a9e647fe.png)


Then, I did <ctrl O> and then <enter> and then <ctrl X>.

## Step 8: Run the tests, demonstrating that they now succeed
```
$ <up arrow> <up arrow> <up arrow> <enter> //should be javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
$ <up arrow> <up arrow> <up arrow> <enter> //should be java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests
```
![image](https://user-images.githubusercontent.com/122569404/221385584-022f9e7d-ac74-42a5-aa71-4f300afcab96.png)

  
## Step 9: Commit and push the resulting change to your Github account
```
$ git add L<tab>.j<tab> //should become ListExamples.java
$ git commit -m "Fixed ListExamples.java"
$ git push origin main
```
  ![image](https://user-images.githubusercontent.com/122569404/221385625-ec6b6f2a-b88c-4b92-b78c-f0ad6ec24ba7.png)

  ## Summary of Command Shortcuts used:
  1. The <tab> will autocomplete a path. If there are multiple paths that fit the pattern, <tab> will autocomplete the path up until the first mismatch.
  2. The <up arrow> will rerun previous commands and it used to scroll up. For example, pressing the <up> 3 times will show the 3rd last command run so far.
  3. The <enter> will run the command after being typed in the terminal.
  
