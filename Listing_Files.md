# Listing Files
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'ls' command to list files present to get desired output.    

## My Solve
**Flag:** 'pwn.college{Yf4fqgnQLndcVn31qJ22_FhFwPz.QX4IDO0wCO1gjNzEzW}'     

Here,it was given that the /challenge/run file was hidden under another name.Hence we use the 'ls' command to list the files present in the directory given as arguement,in this case '/challenge'.By doing so,we chance upon the file '1100-renamed-run-18843' which is the hidden file which upon running gives us the flag ouput.  

'''  
hacker@commands~listing-files:~$ ls /challenge    
1100-renamed-run-18843  DESCRIPTION.md    
hacker@commands~listing-files:~$ /challenge/1100-renamed-run-18843    
Yahaha, you found me! Here is your flag:     
pwn.college{Yf4fqgnQLndcVn31qJ22_FhFwPz.QX4IDO0wCO1gjNzEzW}     
hacker@commands~listing-files:~$     
'''   

## What I learnt
I learnt the usage of the 'ls' command which can be used to see all the files present in the directory given as arguement and as default case,the current directory.   

## References
None.   

<img width="654" height="90" alt="image" src="https://github.com/user-attachments/assets/9e9d76b2-b0f9-47a6-b096-d5c053360f68" />


