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


And here is another example:
```
$ find -name "Bild2*"
$ find -iname "Bild2*"
```
![image](https://user-images.githubusercontent.com/122569404/224590124-59b8e098-5828-4498-aaa4-af9c77b63677.png)

In the first example, I am searching for any file starting with "cse11" (the star is a wildcard character meaning anything that matches can go there). However, using the iname option, I can find files that start with "CSE11" also, since it is case insensitive, widening my search. In the second example, I originally search for any files starting with "Bild2". However, using the iname feature, I can also find files starting with "BILD2". Ulitmately, this feature makes it easier to search for what I want, if I don't remember what the exact upper and lower case letters are in the pattern I am searching for.

## Make Find Show All Files of a Given Type
Another useful feature to refine a search in find is to the use -type feauture. `-type f` is an option to only list files while `-type d` is an option to only list directories. This option is useful if you know whether the thing you are searching for is a directory or a file, and -type will limit the listed results to the option selection

Here is an example:
```
$ find -name "Fiji*" -type d
$ find -name "Fiji*"
```
![image](https://user-images.githubusercontent.com/122569404/224591296-163874e5-56d4-4aa0-9316-91ff903ac16e.png)

And here is another example:
```
$ find -name "style*" -type f
$ find -name "style*"
```
![image](https://user-images.githubusercontent.com/122569404/224591677-640592dd-93a1-49f4-8da0-2d0627a32bda.png)

In the first example, I am able to list all directories starting with "Fiji", rather than including any files starting with "Fiji", making my search more targeted. In the second example, I am able to find all files that start with the word "style", rather than including any directories starting with the word "style". This would be useful if I knew I only wanted directories or files to be listed, helping me refine my search.

## Make Find Show All Files Modified on a Certain Day(s)
A super useful feature of find is to only list files that have been modified on certain days. You can do this using the `-mtime n` option, which would list all files modified n days ago. Doing +n lists all files modified more than n days ago, while doing -n lists all files modified less than n days ago. This is useful if you know the general time period the file you are searching for was last modified.

Here is an example: 
```
$ find -mtime +60
```
![image](https://user-images.githubusercontent.com/122569404/224593920-0f04de46-7274-455e-8e36-02ff9c3f6b4f.png)

And here is another example:
```
$ find -mtime 2
```
![image](https://user-images.githubusercontent.com/122569404/224594085-3445d213-8582-4419-b3bd-d1272d49450d.png)

In the first example, I am searching the working directory (my CSE12 folder) for all files modified more than 60 days ago, since I used +60 as my option for the number of days. In the second example, I am searching the working directory for all files modified exactly 2 days ago, which there are none. This means I hadn't modified any files in that directory exactly 2 days ago. Ultimately, this command is useful if you know the general time period of the last time you or a program modified the file you are searching for.

## Make Find Show All Files Modified at a Certain Minute

TODO: 
This example is somewhat similar to the last example, but instead of searching for files that have been last modified on a certain Day, find also offers a feature to search for files edited a certain number of minutes ago, usiing `find -mmin n`, where n is the number of minutes ago. If you use +n, find searches for files edited more than n minutes ago in the working directory, but if you  choose -n, find searches for files edited less than n minutes ago in the working directory.

Here is an example:
```
$ find -mmin -460
```
![image](https://user-images.githubusercontent.com/122569404/224595707-a3bd86a7-2739-4025-8fe9-071a0bf742f3.png)

And here is another example:
```
$ find -mmin -460 -and -mmin +120
```
![image](https://user-images.githubusercontent.com/122569404/224595773-7c6da969-1bcc-45c0-ba83-028245623d38.png)

In the first example, I list all files that have been modified in the last 460 minutes. In the second examples, I list all files that have been modified between the last 460 minutes and 120 minutes. This gives me much more control on which files I want to search for by choosing files modified by more precise minutes rather than days ago.
