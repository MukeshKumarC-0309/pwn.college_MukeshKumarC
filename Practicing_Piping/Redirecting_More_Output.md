# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '>' command to get the desired output.   

## My Solve
**Flag:** 'pwn.college{YthchGb7eC_OztWAWB7d80gN-0F.QX1YTN0wCO1gjNzEzW}'      

Here we are asked to use the '>' command to redirect the output.So,we know that the '>' is used to redirect the output from one location to another.Here we are supposed to redirect the '/challenge/run' file to 'myflag' file.Hence on using the command '/challenge/run > myflag' it is succesfully redirected.Then on running 'cat myflag' it succesfully prints the flag.    
'''    
Connected!                                                                           
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag    
[INFO] WELCOME! This challenge makes the following asks of you:     
[INFO] - the challenge will check that output is redirected to a specific file path : myflag     
[INFO] - the challenge will output a reward file if all the tests pass : /flag     
      
[HYPE] ONWARDS TO GREATNESS!      
     
[INFO] This challenge will perform a bunch of checks.     
[INFO] If you pass these checks, you will receive the /flag file.     
      
[TEST] You should have redirected my stdout to a file called myflag. Checking...      
      
[PASS] The file at the other end of my stdout looks okay!      
[PASS] Success! You have satisfied all execution requirements.      
hacker@piping~redirecting-more-output:~$ cat myflag      
      
[FLAG] Here is your flag:     
[FLAG] pwn.college{YthchGb7eC_OztWAWB7d80gN-0F.QX1YTN0wCO1gjNzEzW}      
      
hacker@piping~redirecting-more-output:~$      
'''    

## What I Learnt
I learnt further usage of the '>' command where we can redirect one file's contents to another file or some other location.    

## References
None.    

<img width="784" height="309" alt="image" src="https://github.com/user-attachments/assets/a3078f7e-e47f-4b78-94ab-aa811f822837" />




