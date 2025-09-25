# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '--help' argument to get desired output.     

## My Solve
**Flag:** 'pwn.college{ENRzEtBtYAU47DAo0J3COoDkAEz.QX3IDO0wCO1gjNzEzW}'    

Here,we are instructed to run the '/challenge/challenge' command with the '--help' argument to get more details on how to obtain the flag.Hence on doing so we get that we need to get the secret value first with which we can unlock the flag.We use the '-p' argument to get the value.Hence we use the command '/challenge/challenge -p' to get the secret value.Then to print the flag we use the '-g' prompt ie.'/challenge/challenge -g NUM' which in this case was 470 to obtain the ouput ie.the flag value.   
'''  
hacker@man~helpful-programs:~$ /challenge/challenge --help     
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]     
      
optional arguments:     
  -h, --help            show this help message and exit     
  --fortune             read your fortune     
  -v, --version         get the version number     
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG     
                        get the flag, if given the correct value      
  -p, --print-value     print the value that will cause the -g option to give you the flag     
hacker@man~helpful-programs:~$ /challenge/challenge -p     
The secret value is: 470    
hacker@man~helpful-programs:~$ /challenge/challenge -g 470     
Correct usage! Your flag: pwn.college{ENRzEtBtYAU47DAo0J3COoDkAEz.QX3IDO0wCO1gjNzEzW}     
hacker@man~helpful-programs:~$     
'''   

## What I Learnt
I learnt the use of the '--help' argument which can also be used to give more information about the command taken as argument.   

## References
None.   


<img width="652" height="225" alt="image" src="https://github.com/user-attachments/assets/c1eced74-6883-4806-b6ff-6fb811aeeeab" />
