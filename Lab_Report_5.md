# CSE15L Lab Report 5 Researching Commands
Siddharth Gaywala
CSE15L

In this lab report, I completing lab report 3, but exploring the `find` command, unlike last time where I explored the `grep` command.

***
## Make Find Show All Files Matching a Given Name (Case Insensitive)
A useful feature of find is to find all files that match a given name that is case insensitive. You can do this by using the -iname option to tell find to look for files and directories without considering case sensitivity. It is useful in the scenario where you want to find a file with a specific name, but you don't remember if the certain letters of the name of that file are capitalized or not. 
Here is an example:
```
$ find -name "cse11*"
$ find -iname "cse11*"
```
![image](https://user-images.githubusercontent.com/122569404/224589769-ecb70603-de0f-4b97-84d6-2032e9659be5.png)


And here is another example
```
$ find -name "Bild2*"
$ find -iname "Bild2*"
```
![image](https://user-images.githubusercontent.com/122569404/224590124-59b8e098-5828-4498-aaa4-af9c77b63677.png)

In the first example, I am searching for any file starting with cse11 (the star is a wildcard character meaning anything that matches can go there). However, using the iname option, I can find files that start with CSE11 also, since it is case insensitive, widening my search. In the second example, I originally search for any files starting with Bild2. However, using the iname feature, I can also find files starting with BILD2. Ulitmately, this feature makes it easier to search for what I want, if I don't remember what the exact upper and lower case letters are in the pattern I am searching for.

## Make Find Show All Files of a Given Type

## Make Find Show All Files of a certain date

4 options and give 2 examples for each (show each as a code block and command/output) and give sentence about what its doing and why useful
