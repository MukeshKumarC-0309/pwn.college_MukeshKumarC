# Changing Permissions
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'chmod' command to get the desired result.      

## My Solve
**Flag:** 'pwn.college{Y26A4iG4Mehky31VTtAiU4wt0VG.QXzcjM1wCO1gjNzEzW}'     

Here,we use the 'chmod' command in the terminal.The 'chmod' command is used to modify file permission to different users in the terminal.It involves specifying which users,what permission and for which file must it be given through arguments.Here we are supposed to read the '/file' but we as hackers haven't been given permission to read the file.Hence we use the command,'chmod go+r /flag' to add read permissions for all users.Then we can run '/flag' to read the flag output.       
'''      
Connected!                                                                              
hacker@permissions~changing-permissions:~$ ls -l /flag      
-r-------- 1 root root 60 Sep 29 14:53 /flag                
hacker@permissions~changing-permissions:~$ chmod go+r /flag          
hacker@permissions~changing-permissions:~$ ls -l /flag         
-r--r--r-- 1 root root 60 Sep 29 14:53 /flag           
hacker@permissions~changing-permissions:~$ cat /flag          
pwn.college{Y26A4iG4Mehky31VTtAiU4wt0VG.QXzcjM1wCO1gjNzEzW}         
hacker@permissions~changing-permissions:~$            
'''        

## What I Learnt
I learnt the use of 'chmod' command which can be used to modify file permissions for different users according to the arguments given in the terminal.       

## References
None.        


<img width="747" height="133" alt="image" src="https://github.com/user-attachments/assets/5cb215f7-caaa-49e6-84a7-132e34a97e1c" />
