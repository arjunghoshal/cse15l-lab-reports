# Lab Report 1 Week 2  

## Step 1: Installing VSCode  
To install VSCode, download it from the [VSCode Site](https://code.visualstudio.com/). You should see a webpage similar to the one shown below.  
![Step 1-1](/cse15l-lab-reports/images/lab-report-1-step-1-1.PNG)  
  
Click the download button, open the installer, and follow the instructions to download VSCode. When the following screen shows, make sure to select the outlined options.  
![Step 1-2](/cse15l-lab-reports/images/lab-report-1-step-1-2.png)  

Finally, open VSCode. You should see a screen like this:
![Step 1-3](/cse15l-lab-reports/images/lab-report-1-step-1-3.PNG)

## Step 2: Remotely Connecting
Use ssh to connect to the `ieng` servers in the CSE basement. Use the following command in the VSCode terminal to connect:  
`ssh cs15lwi22ann@ieng6.ucsd.edu`  
![Step 2](/cse15l-lab-reports/images/lab-report-1-step-2.PNG)  
Enter your password. If it asks for confirmation the first time, say yes.  

## Step 3: Trying Some Commands
Once in the `ieng` servers, try some commands on the remote machine. Some basic commands are:  
`ls` to view the contents of the current directory  
`cd` to change directories  
`pwd`  to print the current directory  
![Step 3](/cse15l-lab-reports/images/lab-report-1-step-3.PNG)  

## Step 4: Moving Files with `scp`
We can transfer files between the local and remote machine using the `scp` command. Exit the remote machine and try transferring a file to it using the following command:  
`scp sourcefile.txt cs15lwi22ann@ieng6.ucsd.edu:~/`  
![Step 4](/cse15l-lab-reports/images/lab-report-1-step-4.PNG)  
In the image above I transferred the `WhereAmI.java` file from my local machine to the remote machine, connected to the remote machine, then compiled and ran the java program on the remote machine.

## Step 5: Setting an SSH Key
Setting an SSH key will allow you to not enter your password every time you connect or transfer something to the remote machine. This speeds up the process tremendously. To create an ssh key, run `ssh-keygen` on your local machine.  
![Step 5-1](/cse15l-lab-reports/images/lab-report-1-step-5-1.PNG)
A private and public key will have been generated in the `.ssh/` directory. `cd` to the `.ssh/` directory and transfer the id_rsa.pub file to the remote machine's `~/.ssh/authorized_keys` file using `scp`. The process is shown below.  
![Step 5-2](/cse15l-lab-reports/images/lab-report-1-step-5-2.PNG)  
As can be seen in the image, after this, you should be able to log in to the remote machine without a password

## Step 6: Optimizing Remote Running
In order to make our programming process more efficient, we must make the remote running process faster. We have already done so with the ssh key step, however, further improvements can be made.  
![Step 6](/cse15l-lab-reports/images/lab-report-1-step-6.PNG)  
As can be seen above, I have made my process more efficient by combining the transfer, login, compiling, and running steps into one command. Thus my running process is comprised of just 2 keystrokes: pressing up arrow on the terminal, and pressing enter. This is fast, but you can make it even more efficient in other ways, such as creating a script for easy running and testing.