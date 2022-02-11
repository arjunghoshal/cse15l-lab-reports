# Lab Report 3 Week 6  
  
## Streamlining ssh Configuration:  
In order to make accessing my course account easier, I streamlined my ssh config such that I can use the alias `ieng6` to log in to my course account.  

![SSH Config File](/cse15l-lab-reports/images/lab-report-3-1.PNG)  

As can be seen from the config file, I have set the alias to `ieng6`. This along with the previous public key optimization that we did in a previous lab means that I can log into my couse account without a password or long command. For example:  

![SSH Login](/cse15l-lab-reports/images/lab-report-3-2.PNG)  
![SCP Transfer](/cse15l-lab-reports/images/lab-report-3-3.PNG)  

As can be seen from the images above, I no longer need to enter a password or long command to use my course account. the `ssh ieng6` command directly logs me in and the `scp <source> ieng6:<destination>` command directly transfers a file. No more long commands!