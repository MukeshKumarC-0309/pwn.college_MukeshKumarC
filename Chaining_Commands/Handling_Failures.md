# Handling Failures
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '||' command to get the desired output.

## My Solve
**Flag:** 'pwn.college{klBoQtoLAJH05_uIaNz1OKUcjTf.01M0MDOxwCO1gjNzEzW}'           

Here,we use the '||' command in the terminal.The '||' command acts as an OR operator wherein the second command is exceuted only if the first one fails.Here we are asked to check two commands '/challenge/first-failure' and '/challenge/second'.Hence we use '/challenge/first-failure || /challenge/second' to check if they run or not,getting the flag value successfully.       
'''       
Connected!                                                                                
hacker@chaining~handling-failure:~$ /challenge/first-failure || /challenge/second         
Nice chaining! Flag: pwn.college{klBoQtoLAJH05_uIaNz1OKUcjTf.01M0MDOxwCO1gjNzEzW}          
hacker@chaining~handling-failure:~$         
'''       

## What I Learnt 
I learnt the use of '||' command which acts as an OR operator which executes the second command only if the first one fails.     

## References
None.      


<img width="636" height="64" alt="image" src="https://github.com/user-attachments/assets/10d197d5-774f-427e-898d-8d4d658595fa" />
