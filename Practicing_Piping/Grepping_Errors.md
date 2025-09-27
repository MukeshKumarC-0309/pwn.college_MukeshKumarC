# Grepping Errors
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'grep' command with redirection to get the desired output.    

## My Solve
**Flag:** 'pwn.college{guZm8pziOfT_baopwvtb-tB8Y9k.QX1ATO0wCO1gjNzEzW}'

Here,we are asked to redirect the error output and grep for files at the same time.Since it’s not possible with the usual '>' command with pipe,we have to use another alternative ie. '>&' which redirects a file descriptor to another file descriptor.we are going to usee 2>&1 which indicates standard error passed to standard output(2 stands for error and 1 stands for output),and then create a pipe to use 'grep' to filter out the flag.Hence our final command ie.' /challenge/run 2>&1|grep 'pwn.college'' when run gives us the final output(flag value).   
'''     
Connected!                                                                           
hacker@piping~grepping-errors:~$ /challenge/run 2>&1|grep 'pwn.college'       
[INFO] WELCOME! This challenge makes the following asks of you:      
[INFO] - the challenge checks for a specific process at the other end of stderr : grep     
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt     
     
[HYPE] ONWARDS TO GREATNESS!     

[INFO] This challenge will perform a bunch of checks.      
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.     
       
[TEST] You should have redirected my stderr to another process. Checking...      
[TEST] Performing checks on that process!      
        
[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.        
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).       
[INFO] To pass the checks, the executable must be grep.      
       
[PASS] You have passed the checks on the process on the other end of my stderr!        
[PASS] Success! You have satisfied all execution requirements.      
pwn.college{guZm8pziOfT_baopwvtb-tB8Y9k.QX1ATO0wCO1gjNzEzW}      
hacker@piping~grepping-errors:~$       
'''    

## What I Learnt
I learnt the use of the '>&' command which helps us bypass the issue of redirecting errors and can help us achieve that even with the use of a pipe.   

## References
None.     

<img width="1055" height="321" alt="image" src="https://github.com/user-attachments/assets/b4710d72-667c-4957-93c0-907ce2d82cb5" />

