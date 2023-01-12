# CSE15L Lab Report 1: How to log-on to ieng6
This tutorial is for new CSE15L students trying to log onto their course specific account.

***
## Installing VS Code
You will want to use Visual Studio Code as the program to type up code for this class. Let's download VS Code.
1. Go to the Visual Studio Code Website (https://code.visualstudio.com/)
2. Download & install the newest version of VS Code based on your operating system
3. Some of you will already have VS Code installed for a previous class (like I did), in which case you may not need to redownload VS Code as long as you have the correct version.
![image](https://user-images.githubusercontent.com/122569404/212181766-9d9c8071-3ac6-4b4a-8cd2-467de941befa.png)
>Sample Image of VS Code downloaded
***
## Remote Connecting
You will want to connect to the remote server for this class as a place to store code you type up and work on projects. Let's connect to the remote server.
(Steps 2-3 not necessary if on Mac)
1. Set up your CSE15L account on the UCSD Website (https://sdacs.ucsd.edu/~icc/index.php). You can do this by logging in, clicking on the "cs15lwi23xxx" button, and changing your password. To change your password, make sure to hit enter and not hit the blue button. Wait 15 minutes so the account password change can sync.
2. Install Git for Windows (https://gitforwindows.org/)
3. Follow this [tutorial][1] to get Git connected with VS Code
4. If the terminal is not open, press Cnrl + ` to open the terminal.
5. Enter the following command (without the $)
`$ ssh cs15lwi23zz@ieng6.ucsd.edu`
6. Type yes and press enter.
7. Now, enter the password you had set in step 1. Your output should look similar to the image.
![image](https://user-images.githubusercontent.com/122569404/212183831-b6b3a0c8-c7c0-4dac-9f4f-08b21b2044ef.png)
>Sample input and output in the terminal to remote connect.

[1]: [https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994]

***
## Using Commands
You will be using the terminal in this class to open files, run files, move files, and run commands in this class. Let's try some common commands.
* cat {path} {path2}: prints contents of those files
> {path} can be absolute path or relative path (relative path just appends to current directory)
* ls {path}: lists files/folders in given path
* pwd: prints working directory
* cd {path}: change directory, can be {..} to go to parent

![image](https://user-images.githubusercontent.com/122569404/212184896-cbf315bf-6293-4cf0-b1cb-f8d45c2349bc.png)
> For example, I run some commands to cat (print contents of hello.txt), pwd (show working directory), and ls (to show files in my current working directory).
