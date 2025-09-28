# Suspending Process
The challenge asks you to open the terminal in the pwn.college DOJO and invoke control+z to get the desired output.   

## My Solve
**Flag:** 'pwn.college{whsRk-dIs4gkZaJ9o_XwFf7eq36.QX1QDO0wCO1gjNzEzW}'     

Here,we are asked to have '/challenge/run' twice for the challenge to be completed.Hence we can use control+z to suspend one of the two processes to let it run in the background.Hence first we run '/challenge/run' and control+z to let it run in the background.Running the same command again gives you the output.     
'''      
Connected!                                                                               
hacker@processes~suspending-processes:~$ /challenge/run      
I'll only give you the flag if there's already another copy of me running in       
this terminal... Let's check!       

UID          PID    PPID  C STIME TTY          TIME CMD     
root         372     173  0 18:53 pts/0    00:00:00 bash /challenge/run     
root         374     372  0 18:53 pts/0    00:00:00 ps -f        

I don't see a second me!     
       
To pass this level, you need to suspend me and launch me again! You can       
background me with Ctrl-Z or, if you're not ready to do that for whatever        
reason, just hit Enter and I'll exit!      
^Z      
[1]+  Stopped                 /challenge/run      
hacker@processes~suspending-processes:~$ /challenge/run       
I'll only give you the flag if there's already another copy of me running in       
this terminal... Let's check!        
        
UID          PID    PPID  C STIME TTY          TIME CMD       
root         372     173  0 18:53 pts/0    00:00:00 bash /challenge/run       
root         379     173  0 18:53 pts/0    00:00:00 bash /challenge/run       
root         381     379  0 18:53 pts/0    00:00:00 ps -f      
       
Yay, I found another version of me! Here is the flag:      
pwn.college{whsRk-dIs4gkZaJ9o_XwFf7eq36.QX1QDO0wCO1gjNzEzW}      
hacker@processes~suspending-processes:~$       
'''     


## What I Learnt 
I learnt the usage of control+z which is used to suspend processes and let them run in the background.        

## References
None.       

<img width="747" height="408" alt="image" src="https://github.com/user-attachments/assets/e862b174-113a-43ff-ad80-6c4cb9f6f030" />


