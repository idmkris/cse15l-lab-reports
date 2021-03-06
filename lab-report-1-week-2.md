# **Lab Report Week 2**

This page will briefly talk about how to set up and connect appropriately to one of the server provided by UCSD. In order to do so, we need an IDE. The recommended IDE is Visual Studio Code and here is the walk through of how to installing VS code.
&nbsp;

&nbsp;

## **VSCode installation**

First of all, download VS code at [Link](https://code.visualstudio.com) and follow the instructions to install it on the compuer. After that, you should see a window as below.

![alt text](Screen Shot 2022-01-13 at 7.44.27 PM.png)

If you have windows, you will need to install a program called OpenSSH at [Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse). 

&nbsp;

## **Remotely Connecting**

After, open the terminal in VSCode(Ctrl or Command + ` or open it through the menu bar) and type in the command shown in the picture below whereas auw should be different for other users.

![Image](Screen Shot 2022-01-13 at 8.12.21 PM.png)

Afterward, it will prompt you to enter password to your account. Enter your passwords and you are successfully connected to the server as below.

![Image](Screen Shot 2022-01-06 at 3.25.18 PM.png)

&nbsp;

## **Useful Commands**

Later you can test out different commands such as ```cd``` which help you choose directory and ```ls``` which list all the files in the directory. See below.

![Image](Screen Shot 2022-01-14 at 8.22.52 AM.png)

You can also type ```man ls``` to see the whole list of commands.

![Image](Screen Shot 2022-01-13 at 8.22.10 PM.png)

Personally I tried ```ls -l``` and ```ls --author``` whichever the first one list the file in a long format and the second print authors on top of listing the files in the directory.

![Image](Screen Shot 2022-01-24 at 9.13.40 PM.png)

&nbsp;

## **Move files with scp**

Now we can move files with scp command. Create a file and enter the command in the format below.

![Image](Screen Shot 2022-01-13 at 8.33.38 PM.png)

Use ```ssh``` again to log in and enter ```ls``` again. The file now is moving to server and could be run remotely.

&nbsp;

## **Set up the key**

We can also save the key so that we do not have to enter the password every time. First type ```$ ssh-keygen```. Type /Users/username/.ssh/id_rsa to save the key and eventually you will the photo below.

![Image](Screen Shot 2022-01-13 at 8.42.54 PM.png)

Now connect to the server with ```ssh``` again and type ```mkdir .ssh. Log out the server and type this command -scp /Users/joe/.ssh/id_rsa.pub cs15lwi22@ieng6.ucsd.edu:~/.ssh/authorized_keys``` and substitude the username and the path. After all, you should be able to connect to the server without password like this.

![Image](Screen Shot 2022-01-13 at 8.48.59 PM.png)

&nbsp;

## **Optimization**

We can also optimize remote running by using the command below which can run multiple commands on the same line. For example, in the image below, I used command ```cp``` which copy files to directory. I also used the semicolon after that in the same command to compiles and run the file which saves typing and waiting time. The keystroke of typing command below is ```68``` and it will take extra ```3``` keystrokes(Enter) and waiting time if you enter command separately.

![Image](Screen Shot 2022-01-13 at 8.55.45 PM.png)

You can also use up-arrow to look for the previous command. For example, if you just type the command ```javac WhereAmI.java``` a couple command lines above. You can press the up-arrow key to enter it without typing it. The keystroke of typing ```javac WhereAmI.java``` is ```18``` and up-arrow is only ```1```.