lab_report1.md

# Lab Report Week One

## Installing VScode
![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-30%20at%2011.10.08%20AM.png)

open the website https://code.visualstudio.com/, which is the official website of VScode. After click download bottom on the top of the web page, VScode will begin to download. Click the downloaded file and follow the instructions on the screen. If it was installed on a Mac, go to the system preference and make sure the file just downloaded can be opened. Remember that if the mac is M1 or M2 chips, install the ARM version so it will bcome smooth compare with the x86 version, which can be runned more smoothlly on Apple silicon compared with another version.  

## Remotely Connecting

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/remote%20connect.png)

After resetting the password, we can get in to the remote computer by type in the command (ssh cs15lfa22iu@ieng6.ucsd.edu) in the terminal. Remember, when we are typing our passcode, there is no response on screen, but after we type in the correct passcode, we can get in to the server and see some basic informations. 


## Trying Some Commands
![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-29%20at%203.25.14%20PM.png)


Open the terminal and then we can type in the terminal. It works both in the terminal build in vscode and terminal application build in the computer. The command both works in remote computer and local computer. For example, after we opened the terminal we will see a blank space with only one code which contains the basic information of the device, such as the username. We can put in the command direcetly, some simple command we ahve learned is "ls', which can show every main file folder which includes 'document' and 'desktop'. 'cd' method can help us to do into a file and after we get into a file we can find that the code appear on each new line contains the name of the folder we just get in. In this case, if we type 'ls' again, we can see the file name inside of this folder. 

## Moving Files with scp

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-30%20at%2011.44.46%20AM.png)

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/uploading%20files.png)


running the the cade in the local computer first and see what is the result. In order to let a java file can be runed correctly, we have to use cd instruction to get into the file that the java file is located. After we use javac to compile the java file, we can run the java file by type in java and then name of the file with .java in the end. THen we can see the out put of the file apear on terminal
Then we can upload the file to the remote computer by type in (scp WhereAmI.java cs15lfa22iu@ieng6.ucsd.edu:~/) in the directory we run this java file. We need to type in the passowrd again. After we done that, we can use the ssh command to log into the server and after type in 'ls' in the server terminal (we know we are in the server because the code before the type in box has completely changed) we can see the name of the java file we just upload. Compile the file again and run the code, we can see different result, this result is based on the information of the server rather than the client device(which we are using)

## Setting an SSH Key

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/SSH%20keys.png)

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/step%20of%20SSH.png)

Although we can access to our server remotely right now, but it is frustrating that we need to type in password everytime we want to get in the server. There is a way to avoid those steps in the future. Firstly, we create a two ssh keysm the private one stored on the client and the public one stored on the server. What we need to do is type in '$ ssh-keygen Generating public/private rsa key pair' in the terminal of the client, and then type in the direction of the folder that we want to store our key. The next step is to type in a passcode twice. The device will creat a key for us Then we go to tthe server and type in  "mkdir .ssh", go back to client and type in ' $ scp /Users/joe/.ssh/id_rsa.pub cs15lfa22@ieng6.ucsd.edu:~/.ssh/authorized_keys ', now, we can find that we can access to our server without type in the passcode again and again. We can do this on some other client, include the desktop in the dorm

## Optimizing Remote Running

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/optimizing.png)

Now we can do something more interesting by just do some small modifications of our directions. 
such as log in and list the home directory on the remote server

$ ssh cs15lfa22@ieng6.ucsd.edu "ls"

use semicolons to run multiple commands on the same line in most terminals
One thing we need to always remember is that the server can be acced only when the client is connected to UCSD.protected wifi. Without doing that, we can't do anything related to server we have talked in this lab report. 

