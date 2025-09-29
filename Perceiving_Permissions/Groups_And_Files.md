# Groups and files
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'chgrp' command to get the desired output.    

## My Solve
**Flag:** 'pwn.college{sw34n6x5dZPeuF96vX9zzXO1Flo.QXxcjM1wCO1gjNzEzW}'      

Here,we use the 'chgrp' command in the terminal.The 'chgrp' command is used to change the ownership of a group for a specific file.A group consists of multiple users and 'chgrp' command follows the same syntax as 'chown'.So,we use 'chgrp hacker /flag' to change ownership of the file.After that,if we run the '/flag' file,we get the flag output.       
'''         
Connected!                                                                             
hacker@permissions~groups-and-files:~$ chgrp hacker /flag       
hacker@permissions~groups-and-files:~$ cat /flag             
pwn.college{sw34n6x5dZPeuF96vX9zzXO1Flo.QXxcjM1wCO1gjNzEzW}        
hacker@permissions~groups-and-files:~$        
'''     

## What I Learnt
I learnt the use of 'chgrp' command which is used to change the ownership of a file for a group which includes multiple users.     

## References
None.      


<img width="747" height="81" alt="image" src="https://github.com/user-attachments/assets/387f9536-05c4-46a9-9b77-01e88e2e4eaf" />


