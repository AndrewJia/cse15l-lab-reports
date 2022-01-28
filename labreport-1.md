# Lab Report 1

## Installing VSCode

![Image](./report1-images/InstallingVScode.png)

* Download from the following [link]("https://code.visualstudio.com/download")
* Make sure to get the right version for your operating system

## Remotely Connecting
![Image](./report1-images/RemotelyConnecting.png)

* Using the ssh (secure shell) command
* ssh cs15lwi22zzz@ieng6.ucsd.edu
* where zzz is replaced by your accound info

## Trying Some Commands
![Image](./report1-images/TryingSomeCommands.png)
* Try running cd, ls, pwd, mkdir, and cp
* exit can be used to log out

## Moving Files with scp
![Image](./report1-images/MovingFiles.png)
* Using scp (Secure CoPy)
* Make sure that WhereAmI.java (or whatever file you want) exists on your computer first

## Setting an SSH Key
![Image](./report1-images/sshkeygen.png)
* Generate a ssh key pair to avoid having to type in your password every time
* ssh-keygen generates the keys
* ssh-add for Windows users [here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation)
* Login and run mkdir .ssh to create a .ssh folder on the server, then logout
* scp (location of public key on local computer) cs15lwi22zzz@ieng6.ucsd.edu:~/.ssh/authorized_keys to add public key to server

## Optimizing Remote Running
![Image](./report1-images/optimizingremote.png)
* Commands in quotes after ssh will run the commands, then exit
* Semicolons can be used to run multiple commands on the same line
* cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI
* Previous method: "ssh cs15lwi22zzz@ieng6.ucsd.edu", "PASSWORD", ls (total of 35+ keystrokes)
* New method: copy "ssh cs15lwi22zzz@ieng6.ucsd.edu" (Alt+Tab, Ctl+c-v), type "ls" (total of 10 keystrokes)
* By more than halving the number of keystrokes, remotely running code is more than twice as fast as it was previouslly

## Conclusion
Congrats on making it to the end! <br>
Here's an orange:
![Image](./report1-images/orange.jfif)