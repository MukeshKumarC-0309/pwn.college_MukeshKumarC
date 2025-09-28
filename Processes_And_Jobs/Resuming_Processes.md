# Resuming Processes
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'fg' commands to obtain different results.               

## My Solve
**Flag:** 'pwn.college{4n-VV0HT6OlbqXOzGfKUUK1efPT.QX2QDO0wCO1gjNzEzW}'

Here we use the 'fg' command in the terminal.The 'fg' command is used to resume suspended processes and put them in the foreground.Here we are asked to run '/challenge/run' and suspend it and resume it again.Hence we run '/challenge/run' and then use control+z to suspend it and then use 'fg' command to restart it,completing the challenge giving us the flag.     
'''      
Connected!                                                                             
hacker@processes~resuming-processes:~$ /challenge/run     
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with       
the 'fg' command! Or just press Enter to quit me!      
^Z     
[1]+  Stopped                 /challenge/run      
hacker@processes~resuming-processes:~$ fg        
/challenge/run    
I'm back! Here's your flag:     
pwn.college{4n-VV0HT6OlbqXOzGfKUUK1efPT.QX2QDO0wCO1gjNzEzW}      
Don't forget to press Enter to quit me!      
     
Goodbye!        
hacker@processes~resuming-processes:~$        
'''       

## What I learnt
I learnt the use of 'fg' command which is used to resume suspended processes and continue running them in the forground.      

## References
None.       

<img width="747" height="209" alt="image" src="https://github.com/user-attachments/assets/d0fa96d0-33a1-4335-9bda-0bae990921f2" />
