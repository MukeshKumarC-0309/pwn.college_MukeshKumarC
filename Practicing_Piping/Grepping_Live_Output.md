# Grepping Live output
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'grep' command and pipe operator to obtain the desired output.    

## My Solve
**Flag:** 'pwn.college{0u5Jz45dyCcVcM8OpEjSlvvDyaw.QX5EDO0wCO1gjNzEzW}'      

Here,we are asked to open a file called '/challenge/run' and find the flag among thousands of lines of text.Hence the 'grep' command will be useful.But we are asked to complete the challenge in a single step.This is where the pipe operator comes in. '|' is the pipe operator which is used connect two different commands into one(like a real pipe) hence completing the challenge in a single step.By running ' /challenge/run | grep 'pwn.college''('pwn.college' is present in all flags),we complete the challenge and get the flag value successfully.   
'''       
Connected!                                                                            
hacker@piping~grepping-live-output:~$ /challenge/run | grep 'pwn.college'      
[INFO] WELCOME! This challenge makes the following asks of you:      
[INFO] - the challenge checks for a specific process at the other end of stdout : grep     
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt      
       
[HYPE] ONWARDS TO GREATNESS!      
      
[INFO] This challenge will perform a bunch of checks.      
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.     
      
[TEST] You should have redirected my stdout to another process. Checking...     
[TEST] Performing checks on that process!      
     
[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.     
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).     
[INFO] To pass the checks, the executable must be grep.    
     
[PASS] You have passed the checks on the process on the other end of my stdout!     
[PASS] Success! You have satisfied all execution requirements.     
pwn.college{0u5Jz45dyCcVcM8OpEjSlvvDyaw.QX5EDO0wCO1gjNzEzW}     
hacker@piping~grepping-live-output:~$      
'''   

## What I Learnt
I learnt the use of the pipe operator denoted by '|' which is used as a pipe to connect two different commands such that the output of the first command is taken as the input of the second command.     

## References
None.    

<img width="1055" height="321" alt="image" src="https://github.com/user-attachments/assets/1bc35588-f9fa-4253-8ba8-15357042fffa" />

