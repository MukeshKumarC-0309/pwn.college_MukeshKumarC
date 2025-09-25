# Help For Builtins
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the help command(builtin) to get the desired output.   
## My Solve
**Flag:** 'pwn.college{8yVf40kJCDaZBu31EvwbUtRcKrK.QX4YjM1wCMxAzNzEzW}'    

Here we use the 'help' builtin with the 'challenge' command.The 'help' builtin is also similar to the '--help' argument which gives us more details about the command.Here,on using the 'help challenge' command,we get all the details about the command,including the one where we need to use the '--secret VALUE' argument to get the flag.Hence we use the 'challenge --secret EFKbbJGl' command(the value is EFKbbJHl) and succefully retrieve the flag.   
'''    
hacker@man~help-for-builtins:~$ help challenge      
challenge: challenge [--fortune] [--version] [--secret SECRET]      
    This builtin command will read you the flag, given the right arguments!      
    
    Options:      
      --fortune		display a fortune      
      --version		display the version     
      --secret VALUE	prints the flag, if VALUE is correct    
        
    You must be sure to provide the right value to --secret. That value        
    is "EFKbbJGl".      
hacker@man~help-for-builtins:~$ challenge --secret EFKbbJGl      
Correct! Here is your flag!      
pwn.college{EFKbbJGlRqVpxTUSkN_ndEuvGRb.QX0ETO0wCO1gjNzEzW}      
hacker@man~help-for-builtins:~$       
'''    

## What I Learnt
I learnt the use of the 'help' builtin which can tell us more about the commands given as argument which can help us unlock hidden clues to obtain the flag.   

## References
None.

<img width="652" height="204" alt="image" src="https://github.com/user-attachments/assets/0672f374-cc43-480f-b407-8a18b47fbb7a" />    

<img width="418" height="33" alt="image" src="https://github.com/user-attachments/assets/79f8afd0-5110-409f-9a82-ca29397c1691" />

