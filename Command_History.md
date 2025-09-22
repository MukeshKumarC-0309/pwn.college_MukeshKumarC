# Command History
The challenge asks you to open the terminal in the pwn.college DOJO and use the 'history' feature(involving using the right arrow) to obtain the flag

## My Solve
**Flag:** 'pwn.college{MZXTqmh02UAC2WChZxY6mOlkCXC.0lNzEzNxwCO1gjNzEzW}'

Here we learn that linux is able to save all the codes we have typed so far in its 'history' which can be accessed by clicking the right arrow.Hence we do that because the flag is hidden in the history.While doing so we obtain the flag.  

'''  
hacker@paths~the-root:~$ /pwn   
BOOM!!!    
Here is your flag:   
pwn.college{EvHvRrsXCgAbRUp5uLOT2_VJ8qb.QX4cTO0wCO1gjNzEzW}    
hacker@paths~the-root:~$       
'''     

## What I learnt
I learnt that when we type lots of code,we can always access the previous using the 'history' feature which makes accessing commands much easier  

## References
None.

<img width="753" height="19" alt="Screenshot 2025-09-22 at 7 25 09 PM" src="https://github.com/user-attachments/assets/6188f15b-8e26-401b-94bb-58be049e45a2" />

