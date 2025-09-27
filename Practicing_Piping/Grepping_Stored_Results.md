# Grepping Stored Results
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'grep' command to get the desired output.    

## My Solve
**Flag:** 'pwn.college{EWRpJ7Ji5p-RoaAud-wtXUME0db.QX4EDO0wCO1gjNzEzW}'      

First we execute the output redirection from '/challenge/run' to '/tmp/data.txt' using the '>' command by the command '/challenge/run > /tmp/data.txt'.Once it’s successfully completed,we need to find the flag from the file.But since the file contains thousands of lines of text,it's manually impossible to find the flag.Hence we use the grep command with 'pwn.college' as the argument since all flags start with that phrase.Hence on using 'grep "pwn.college" /tmp/data.txt' we successfully retrieve the flag value.    
'''   
Connected!                                                                           
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt      
[INFO] WELCOME! This challenge makes the following asks of you:     
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt      
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt     
      
[HYPE] ONWARDS TO GREATNESS!     
      
[INFO] This challenge will perform a bunch of checks.      
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.     
      
[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...     
       
[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.      
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are     
[HINT] creating and trying to pass in FDs in python.     
      
[PASS] The file at the other end of my stdout looks okay!    
[PASS] Success! You have satisfied all execution requirements.    
hacker@piping~grepping-stored-results:~$ grep "pwn.college" /tmp/data.txt   
pwn.college{EWRpJ7Ji5p-RoaAud-wtXUME0db.QX4EDO0wCO1gjNzEzW}    
hacker@piping~grepping-stored-results:~$     
'''     


## What I Learnt
We learnt the use of 'grep' command to filter through large files to find the required information and the '>' command which is used for output redirection.   

## References
None.    

<img width="863" height="321" alt="image" src="https://github.com/user-attachments/assets/3e506b06-65ee-4f87-9d2c-94b4b337b447" />

