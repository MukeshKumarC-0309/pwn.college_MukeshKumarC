# Backgrounding Processes
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'bg' command to get the desired output.     

## My Solve
**Flag:** 'pwn.college{k4-11xA0tU6xemanLEcB7NjaNd3.QX3QDO0wCO1gjNzEzW}'      

Here,we use the 'bg' command in the terminal.'bg' command is used to run process in the background.Here,we are asked to run 2 copies of '/challenge/run' one in the background and one in the foreground.Hence,we first run '/challenge/run' and then suspend it using control+z and then use the 'bg' command to run it in the backgorund,thus completing the challenge and giving the flag output.      
'''     
Connected!                                                                              
hacker@processes~backgrounding-processes:~$ /challenge/run      
I'll only give you the flag if there's already another copy of me running *and        
not suspended* in this terminal... Let's check!       
     
UID          PID STAT CMD     
root         161 S+   bash /challenge/run     
root         163 R+   ps -o user=UID,pid,stat,cmd     
    
I don't see a second me!     
      
To pass this level, you need to suspend me, resume the suspended process in the      
background, and then launch a new version of me! You can background me with      
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to      
do that for whatever reason, just hit Enter and I'll exit!      
^Z     
[1]+  Stopped                 /challenge/run     
hacker@processes~backgrounding-processes:~$ bg      
[1]+ /challenge/run &      
hacker@processes~backgrounding-processes:~$      
         
       
Yay, I'm now running the background! Because of that, this text will probably       
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times         
to scroll this text out.      
      
hacker@processes~backgrounding-processes:~$ /challenge/run      
I'll only give you the flag if there's already another copy of me running *and      
not suspended* in this terminal... Let's check!      
      
UID          PID STAT CMD       
root         161 S    bash /challenge/run      
root         171 S    sleep 6h      
root         172 S+   bash /challenge/run      
root         174 R+   ps -o user=UID,pid,stat,cmd     
      
Yay, I found another version of me running in the background! Here is the flag:       
pwn.college{k4-11xA0tU6xemanLEcB7NjaNd3.QX3QDO0wCO1gjNzEzW}     
hacker@processes~backgrounding-processes:~$       
'''      

## What I Learnt 
I learnt the use of 'bg' command which is used to run programs in the background.     

## References
None.     

![Uploading image.png…]()

