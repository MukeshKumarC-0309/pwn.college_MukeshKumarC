# Appending Output
The challenge asks you to open the terminal in the pwn.college DOJO and use the '>>' command to get desired output.   

## My Solve
**Flag:** 'pwn.college{g7JHSoTySiAFw68RdNj5Knu8x5_.QX3ATO0wCO1gjNzEzW}'   

Here,first we are asked to append the '/challenge/run' file to the '/home/hacker/the-flag'.However it says that we should append it and not redirect it as redirecting will split the flag into 2 different locations,rendering the '>' command invalid.Hence we use the append command denoted by '>>' which doesn’t overwrite on the file and instead just appends it from the end.Hence running the command '/challenge/run >> /home/hacker/the-flag' succefully appends the file to the required location.Then upon running the command 'cat /home/hacker/the-flag' to run the file,it gives us the flag output.    
'''   
Connected!                                                                           
hacker@piping~appending-output:~$ /challenge/run >> /home/hacker/the-flag    
[INFO] WELCOME! This challenge makes the following asks of you:      
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag      
      
[HYPE] ONWARDS TO GREATNESS!       
      
[INFO] This challenge will perform a bunch of checks.      
[INFO] Good luck!      
      
[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...      

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.        
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are      
[HINT] creating and trying to pass in FDs in python.       

[PASS] The file at the other end of my stdout looks okay!     
[PASS] Success! You have satisfied all execution requirements.     
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do      
the first write directly to the file, and the second write, I'll do to stdout     
(if it's pointing at the file). If you redirect the output in append mode, the     
second write will append to (rather than overwrite) the first write, and you'll          
get the whole flag!            
hacker@piping~appending-output:~$ cat /home/hacker/the-flag             
 |      
\|/ This is the first half:     
 v      
pwn.college{g7JHSoTySiAFw68RdNj5Knu8x5_.QX3ATO0wCO1gjNzEzW}     
                              ^     
     that is the second half /|\      
                              |     

If you only see the second half above, you redirected in *truncate* mode (>)      
rather than *append* mode (>>), and so the write of the second half to stdout     
overwrote the initial write of the first half directly to the file. Try append     
mode!       
hacker@piping~appending-output:~$       
'''    


## What I Learnt
I learnt the usage of the append command denoted by '>>' which is used ti append the file to a new location instead of overwriting over an existing file,if any.    

## References
None.    


<img width="899" height="538" alt="image" src="https://github.com/user-attachments/assets/31e48395-5dd3-4fb9-a975-b890ad2b47ec" />


