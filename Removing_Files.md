# Removing Files
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'rm' command to get the desired output.  

## My Solve
**Flag:** 'pwn.college{QNHwwqq8e1t38R-BnwRYLIbytVU.QX2kDM1wCO1gjNzEzW}'  

First,we execute the 'rm' command in the terminal.The 'rm' command is used to delete files from the directory.Here,we are instructed to delete the file 'delete_me' and then we run the 'challenge/check' command and we get our flag.  
'''  
hacker@commands~removing-files:~$ rm delete_me   
hacker@commands~removing-files:~$ /challenge/check    
Excellent removal. Here is your reward:   
pwn.college{QNHwwqq8e1t38R-BnwRYLIbytVU.QX2kDM1wCO1gjNzEzW}   
hacker@commands~removing-files:~$   
'''  

## What I learnt
I learnt the use of the 'rm' command which is used to delete the files,the file name is given as the arguement from the directory.  

## References
None.   

<img width="654" height="90" alt="image" src="https://github.com/user-attachments/assets/6fcf1393-b3c8-4b48-b9d3-f339fce352ca" />


