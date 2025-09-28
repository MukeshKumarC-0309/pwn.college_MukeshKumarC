# Interrupting Files 
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'ctrl+c' command to get the desired output.      

## My Solve
**Flag:** 'pwn.college{81pfrSHPlZfk4DbXZ-NfpsBZdqI.QXzQDO0wCO1gjNzEzW}'    

Here,we are asked to run '/challenge/run' to get the flag,but when we run it,it tells us that it won’t give us the flag until we interrupt it.This can be done by pressing control+c which can interrupt a process in the middle of it happening.Hence when we press control+c,the process is stopped midway succesfully completing the challenge,giving us our flag.     
'''     
Connected!                                                                             
hacker@processes~interrupting-processes:~$ /challenge/run     
I could give you the flag... but I won't, until this process exits. Remember,      
you can force me to exit with Ctrl-C. Try it now!      
^C      
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:      
pwn.college{81pfrSHPlZfk4DbXZ-NfpsBZdqI.QXzQDO0wCO1gjNzEzW}     
hacker@processes~interrupting-processes:~$      
'''    

## What I Learnt
I learnt the use of control+c command which can be used to interrupt a program from completing incase there's any error or is going on an infinite loop.     

## References
None.         


<img width="629" height="122" alt="image" src="https://github.com/user-attachments/assets/c93733f6-73d0-4ad9-87ea-fd633b1e7362" />
