# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'fg' command to get the desired output.       

## My Solve
**Flag:** 'pwn.college{oFT9MLAcWhsBzbLpIbDByXr85eW.QX4QDO0wCO1gjNzEzW}'    

Here we use the 'fg' command in the terminal.The 'fg' command is used to run the background processes in the foreground.Here,we are asked to background the process '/challenge/run' and then foreground it.So first we run '/challenge/run' and then suspend it using control+z and then run it in the background using the 'bg' command.Finally we use the 'fg' command to run the command in the foreground,completing the challenge and getting the flag output.      
'''      
Connected!     
hacker@processes~foregrounding-processes:~$ /challenge/run     
To pass this level, you need to suspend me, resume the suspended process in the     
background, and *then* foreground it without re-suspending it! You can       
background me with Ctrl-Z (and resume me in the background with 'bg') or, if        
you're not ready to do that for whatever reason, just hit Enter and I'll exit!      
^Z    
[1]+  Stopped                 /challenge/run      
hacker@processes~foregrounding-processes:~$ bg      
[1]+ /challenge/run &      
hacker@processes~foregrounding-processes:~$      
       
      
Yay, I'm now running the background! Because of that, this text will probably      
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times      
to scroll this text out. After that, resume me into the foreground with 'fg';      
I'll wait.     
     
hacker@processes~foregrounding-processes:~$ fg    
/challenge/run      
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!     
    
pwn.college{oFT9MLAcWhsBzbLpIbDByXr85eW.QX4QDO0wCO1gjNzEzW}        
hacker@processes~foregrounding-processes:~$          
'''     

## What I Learnt
I learnt the use of 'fg' command which can be used to run the background processes in the foreground.      

## References 
None.      


<img width="747" height="337" alt="image" src="https://github.com/user-attachments/assets/d7a1160d-3f99-4c1a-abd5-1322d73ba842" />
