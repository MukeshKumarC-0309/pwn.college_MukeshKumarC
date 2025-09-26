# Linking Files
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'rm' and 'ln -s' command to obtain desired result.   

## My Solve
**Flag:** 'pwn.college{EYW8xkKxynjB9LAKqLniiW26qCN.QX5ETN1wCO1gjNzEzW}'  

Here,we are instructed to run the 'challenge/catflag' command but is instead redirected to the '/home/hacker/not-the-flag' command which is just a random file.Hence we remove the original file using the 'rm' command.Then we link the '/flag' file which contains the flag value with the '/home/hacker/not-the-flag' file using a soft link ie.'ln -s' command.Then upon running the '/challenge/catflag' command,it redirects to the '/home/hacker/not-the-flag' file which now contains the flag value.  
'''  
hacker@commands~linking-files:~$ rm /home/hacker/not-the-flag     
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag      
hacker@commands~linking-files:~$ /challenge/catflag      
About to read out the /home/hacker/not-the-flag file!      
pwn.college{EYW8xkKxynjB9LAKqLniiW26qCN.QX5ETN1wCO1gjNzEzW}     
hacker@commands~linking-files:~$      
'''    

## What I Learnt
I learnt the use of linking files as it allows to bypass certain imitations and access the required files,using the 'ln -s' command.    

## References
None.

<img width="626" height="90" alt="image" src="https://github.com/user-attachments/assets/cbeb545c-7b17-41d6-a3d3-0685e3964768" />
