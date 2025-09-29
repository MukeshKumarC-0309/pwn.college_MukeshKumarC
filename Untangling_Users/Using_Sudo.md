# Using sudo
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'sudo' commands to obtain desired result.    

## My Solve
**Flag:** 'pwn.college{I3WQBPFur2Deo8vqIyiFQlhMGcy.QX4UDN1wCO1gjNzEzW}'         

Here,we are asked to use 'sudo' command in the terminal.The 'sudo' command which stands for superuser do gives us access to all commands when used.Here to open the file '/flag',we use 'sudo cat /flag' to access the file which gives us the flag output.      
'''       
Connected!                                                                           
hacker@users~using-sudo:~$ sudo cat /flag       
pwn.college{I3WQBPFur2Deo8vqIyiFQlhMGcy.QX4UDN1wCO1gjNzEzW}        
hacker@users~using-sudo:~$           
'''     

## What I Learnt
I learnt the use of the 'sudo' command which gives temporary access to all commands according to the policies to the user.       

## References
None.      

<img width="747" height="67" alt="image" src="https://github.com/user-attachments/assets/234092f7-aecd-4a64-81de-d9353b5140c5" />

