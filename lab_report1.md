lab_report1.md

# Lab Report Week One

## Installing VScode
![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-30%20at%2011.10.08%20AM.png)

the whole process is pretty easy, just remember that if the mac is M1 or m2 chips, install the ARM version so it will bcome smooth compare with the x86 version

## Remotely Connecting

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/remote%20connect.png)

After resetting the password, we can get in to the remote computer by type in the command (ssh cs15lfa22iu@ieng6.ucsd.edu)


## Trying Some Commands
![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-29%20at%203.25.14%20PM.png)


Open the terminal and then we can type in the terminal. It works both in the terminal build in vscode and terminal application build in the computer. The command both works in remote computer and local computer. 

## Moving Files with scp

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/Screen%20Shot%202022-09-30%20at%2011.44.46%20AM.png)

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/uploading%20files.png)


running the the cade in the local computer first and see what is the result. 
Then we can upload the file to the remote computer by type in (scp WhereAmI.java cs15lfa22iu@ieng6.ucsd.edu:~/) in the directory we run this java file

## Setting an SSH Key

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/SSH%20keys.png)

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/step%20of%20SSH.png)

after we creat a public and a private key and store in our client and server computer, we can access to the server without type in the password. 

## Optimizing Remote Running

![Image](https://github.com/Kevinxsn/cse15l-lab-reports/blob/main/optimizing.png)

Now we can do something more interesting by just do some small modifications of our directions. 
such as log in and list the home directory on the remote server

$ ssh cs15lfa22@ieng6.ucsd.edu "ls"



use semicolons to run multiple commands on the same line in most terminals

