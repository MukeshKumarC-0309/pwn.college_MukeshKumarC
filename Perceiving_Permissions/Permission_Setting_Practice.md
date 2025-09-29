# Permission Setting Practice
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'chmod' command to get the desired output.    

## My Solve
**Flag:** 'pwn.college{oF4uB5wu7iO_3gvPZ1qO049w1r3.QXzETO0wCO1gjNzEzW}'     

Here,we use the 'chmod' command in the terminal.The 'chmod' command is used to modify file permissions for different types of users.Unlike previous challenges,we can also preset permissions using the 'chmod' command and '=/-' operators to set up permissions.Here,we are tasked with modifying the file permission 8 different times for us to unlock the file.Hence once unlocked we see that the '/flag' file has no permissions.Hencewe enable read permissions for all so that we can read the '/flag' file getting the flag output.    
'''      
Connected!                                                                           
hacker@permissions~permissions-setting-practice:~$ /challenge/run   
Round 1 of 8!    
   
Current permissions of "/challenge/pwn": rw-r--r--   
* the user does have read permissions   
* the user does have write permissions   
- the user doesn't have execute permissions   
* the group does have read permissions   
- the group doesn't have write permissions   
- the group doesn't have execute permissions   
* the world does have read permissions  
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
    
Needed permissions of "/challenge/pwn": rwx----w-   
* the user does have read permissions    
* the user does have write permissions    
* the user does have execute permissions   
- the group doesn't have read permissions   
- the group doesn't have write permissions  
- the group doesn't have execute permissions   
- the world doesn't have read permissions   
* the world does have write permissions   
- the world doesn't have execute permissions   
hacker@permissions~permissions-setting-practice:~$ chmod u=rwx,g=-,o=w /challenge/pwn   
You set the correct permissions!    
Round 2 of 8!    
   
Current permissions of "/challenge/pwn": rwx----w-    
* the user does have read permissions    
* the user does have write permissions   
* the user does have execute permissions   
- the group doesn't have read permissions   
- the group doesn't have write permissions      
- the group doesn't have execute permissions   
- the world doesn't have read permissions   
* the world does have write permissions   
- the world doesn't have execute permissions   
   
Needed permissions of "/challenge/pwn": rwx-wx---   
* the user does have read permissions   
* the user does have write permissions   
* the user does have execute permissions   
- the group doesn't have read permissions   
* the group does have write permissions   
* the group does have execute permissions   
- the world doesn't have read permissions   
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
hacker@permissions~permissions-setting-practice:~$ chmod u=rwx,g=wx,o=- /challenge/pwn    
You set the correct permissions!    
Round 3 of 8!     
    
Current permissions of "/challenge/pwn": rwx-wx---    
* the user does have read permissions     
* the user does have write permissions     
* the user does have execute permissions   
- the group doesn't have read permissions    
* the group does have write permissions    
* the group does have execute permissions    
- the world doesn't have read permissions   
- the world doesn't have write permissions    
- the world doesn't have execute permissions    
     
Needed permissions of "/challenge/pwn": rwx-wxr--     
* the user does have read permissions    
* the user does have write permissions    
* the user does have execute permissions     
- the group doesn't have read permissions   
* the group does have write permissions    
* the group does have execute permissions   
* the world does have read permissions    
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
hacker@permissions~permissions-setting-practice:~$ chmod u=rwx,g=wx,o=r /challenge/pwn    
You set the correct permissions!    
Round 4 of 8!   
     
Current permissions of "/challenge/pwn": rwx-wxr--    
* the user does have read permissions    
* the user does have write permissions    
* the user does have execute permissions   
- the group doesn't have read permissions   
* the group does have write permissions    
* the group does have execute permissions   
* the world does have read permissions   
- the world doesn't have write permissions    
- the world doesn't have execute permissions    
    
Needed permissions of "/challenge/pwn": r--r---wx     
* the user does have read permissions     
- the user doesn't have write permissions    
- the user doesn't have execute permissions    
* the group does have read permissions   
- the group doesn't have write permissions   
- the group doesn't have execute permissions   
- the world doesn't have read permissions   
* the world does have write permissions   
* the world does have execute permissions   
hacker@permissions~permissions-setting-practice:~$ chmod u=r,g=r,o=wx /challenge/pwn    
You set the correct permissions!   
Round 5 of 8!    
   
Current permissions of "/challenge/pwn": r--r---wx   
* the user does have read permissions   
- the user doesn't have write permissions   
- the user doesn't have execute permissions   
* the group does have read permissions   
- the group doesn't have write permissions   
- the group doesn't have execute permissions   
- the world doesn't have read permissions   
* the world does have write permissions   
* the world does have execute permissions   
   
Needed permissions of "/challenge/pwn": rwx---r-x   
* the user does have read permissions   
* the user does have write permissions   
* the user does have execute permissions  
- the group doesn't have read permissions   
- the group doesn't have write permissions    
- the group doesn't have execute permissions   
* the world does have read permissions    
- the world doesn't have write permissions    
* the world does have execute permissions   
hacker@permissions~permissions-setting-practice:~$ chmod u=rwx,g=-,o=rx /challenge/pwn    
You set the correct permissions!    
Round 6 of 8!    
    
Current permissions of "/challenge/pwn": rwx---r-x    
* the user does have read permissions    
* the user does have write permissions     
* the user does have execute permissions   
- the group doesn't have read permissions   
- the group doesn't have write permissions   
- the group doesn't have execute permissions   
* the world does have read permissions   
- the world doesn't have write permissions   
* the world does have execute permissions   
    
Needed permissions of "/challenge/pwn": -----x--x    
- the user doesn't have read permissions    
- the user doesn't have write permissions   
- the user doesn't have execute permissions     
- the group doesn't have read permissions  
- the group doesn't have write permissions   
* the group does have execute permissions   
- the world doesn't have read permissions   
- the world doesn't have write permissions   
* the world does have execute permissions   
hacker@permissions~permissions-setting-practice:~$ chmod u=-,g=x,o=x /challenge/pwn   
You set the correct permissions!   
Round 7 of 8!   
    
Current permissions of "/challenge/pwn": -----x--x  
- the user doesn't have read permissions   
- the user doesn't have write permissions   
- the user doesn't have execute permissions   
- the group doesn't have read permissions   
- the group doesn't have write permissions   
* the group does have execute permissions   
- the world doesn't have read permissions   
- the world doesn't have write permissions   
* the world does have execute permissions   
    
Needed permissions of "/challenge/pwn": rwxrwx-wx   
* the user does have read permissions    
* the user does have write permissions    
* the user does have execute permissions    
* the group does have read permissions    
* the group does have write permissions    
* the group does have execute permissions    
- the world doesn't have read permissions   
* the world does have write permissions   
* the world does have execute permissions   
hacker@permissions~permissions-setting-practice:~$ chmod u=rwx,g=rwx,o=wx /challenge/pwn   
You set the correct permissions!    
Round 8 of 8!    
    
Current permissions of "/challenge/pwn": rwxrwx-wx    
* the user does have read permissions    
* the user does have write permissions   
* the user does have execute permissions    
* the group does have read permissions   
* the group does have write permissions   
* the group does have execute permissions   
- the world doesn't have read permissions   
* the world does have write permissions   
* the world does have execute permissions   
   
Needed permissions of "/challenge/pwn": r-x----wx   
* the user does have read permissions  
- the user doesn't have write permissions   
* the user does have execute permissions   
- the group doesn't have read permissions   
- the group doesn't have write permissions   
- the group doesn't have execute permissions   
- the world doesn't have read permissions   
* the world does have write permissions   
* the world does have execute permissions   
hacker@permissions~permissions-setting-practice:~$ chmod u=rx,g=-,o=wx /challenge/pwn   
You set the correct permissions!   
You've solved all 8 rounds! I have changed the ownership    
of the /flag file so that you can 'chmod' it. You won't be able to read   
it until you make it readable with chmod!    
    
Current permissions of "/flag": ---------   
- the user doesn't have read permissions    
- the user doesn't have write permissions    
- the user doesn't have execute permissions    
- the group doesn't have read permissions    
- the group doesn't have write permissions     
- the group doesn't have execute permissions    
- the world doesn't have read permissions    
- the world doesn't have write permissions    
- the world doesn't have execute permissions     
hacker@permissions~permissions-setting-practice:~$ chmod a+r /flag     
hacker@permissions~permissions-setting-practice:~$ cat /flag      
pwn.college{oF4uB5wu7iO_3gvPZ1qO049w1r3.QXzETO0wCO1gjNzEzW}       
hacker@permissions~permissions-setting-practice:~$
'''

## What I Learnt
I learnt the use of 'chmod' command along with '=/-' operators which can be used to preset file permissions for different types of users.        

## References
None.     

<img width="611" height="900" alt="image" src="https://github.com/user-attachments/assets/159630e7-62ec-4c76-9567-4832d0bf33bf" />    


<img width="611" height="900" alt="image" src="https://github.com/user-attachments/assets/c8fa00c7-bfe9-41b6-bf6b-024c29eebf69" />   


<img width="636" height="900" alt="image" src="https://github.com/user-attachments/assets/d9a83f52-6535-4fe2-995d-78a878db9d21" />   


<img width="636" height="789" alt="image" src="https://github.com/user-attachments/assets/2cc396de-bdc3-4fed-90e8-aaff7d8897b0" />




