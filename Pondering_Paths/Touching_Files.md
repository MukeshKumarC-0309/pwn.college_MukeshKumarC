# Touching Files
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'touch' command to create a new file to get desired output.  

## My Solve
**Flag:** 'pwn.college{QYg46zECcIe6X1DjBPNj5tRq2bn.QXwMDO0wCO1gjNzEzW}'   

The 'touch' command is used to create new text files.Here,we use the 'touch' command to create 2 new files /tmp/pwn and /tmp/college to be saved.then running the '/challenge/run' command gives us the flag.  
'''  
hacker@commands~touching-files:~$ touch /tmp/pwn     
hacker@commands~touching-files:~$ touch /tmp/college    
hacker@commands~touching-files:~$ /challenge/run    
Success! Here is your flag:      
pwn.college{QYg46zECcIe6X1DjBPNj5tRq2bn.QXwMDO0wCO1gjNzEzW}       
hacker@commands~touching-files:~$      
'''   

## What I learnt
I learnt the syntax and usage of the 'touch' command which can be used to create new files with the file name as arguement.  

## References
None.

<img width="654" height="90" alt="image" src="https://github.com/user-attachments/assets/f30f2940-ed4f-4f68-a376-697ed429df9a" />


