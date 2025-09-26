# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'echo' and 'hello' commands with multiple arguments to obtain different results.

## My Solve
**Flag:** 'pwn.college{Ifu1Z_KD_MkX0ECHgisy1-iOMaX.0VN0EzNxwCO1gjNzEzW}' 

We use the 'tab' key in the terminal.'Tab' command can also be to autocomplete commands.Here it’s given that the hidden command starts with pwncollege and we must use the tab key to autocomplete it.We see that the hdiden command is 'pwncollege-28682' which gives us the output flag.   
'''  
Connected!                                                                             
hacker@globbing~tab-completion-on-commands:~$ pwncollege-28682       
Correct! Here is your flag:      
pwn.college{Ifu1Z_KD_MkX0ECHgisy1-iOMaX.0VN0EzNxwCO1gjNzEzW}      
hacker@globbing~tab-completion-on-commands:~$      
'''   

## What I learnt
I learnt that we can use the 'tab' key to autocomplete commands also saving us time even in that aspect.    

## References 
None.   

<img width="784" height="97" alt="image" src="https://github.com/user-attachments/assets/b1ea32a6-9df9-4795-89d0-5e95fa005a0e" />




