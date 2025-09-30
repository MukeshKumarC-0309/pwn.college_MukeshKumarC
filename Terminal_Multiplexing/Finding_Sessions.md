# Finding Sessions
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'screen -ls' command to get the desired output.    

## My Solve
**Flag:** 'pwn.college{4pB8bLUlFGrGHlaAUpjpxmnvSaG.01N4IDOxwCO1gjNzEzW}'     

Here,we are asked to find the right screen from a bunch of detached screens.Hence we can use the 'screen -ls' command which shows all the screens in the terminal.Among them,we have to keep trying till we get the right screen.So first,i choose the screen '150.session_e56e54f4537e7e1f' and choose to reattach it.Hence I use 'screen -r session_e56e54f4537e7e1f' and it turns out to be the right screen.Hence it reattaches itself and gives the flag output.        
'''       
Connected!                                                                                  
hacker@terminal-multiplexing~finding-sessions:~$ screen -ls        
There are screens on:        
	323.pts-0.terminal-multiplexing~launching-screen	(Remote or dead)        
	162.pts-0.terminal-multiplexing~detaching-and-attaching	(Remote or dead)        
	144.session_44098d0259934999	(Detached)        
	147.session_071a64b66ec4cfa6	(Detached)        
	150.session_e56e54f4537e7e1f	(Detached)          
5 Sockets in /home/hacker/.screen.        
hacker@terminal-multiplexing~finding-sessions:~$ screen -r session_e56e54f4537e7e1f        
            
            
                  
            
      
          
hacker@terminal-multiplexing~finding-sessions:~$  echo 'Congratulations! You found the right session!'        
Congratulations! You found the right session!    
hacker@terminal-multiplexing~finding-sessions:~$  echo pwn.college{4pB8bLUlFGrGHlaAUpjpxmnvSaG.01N4IDOxwCO1gjNzEzW}        
pwn.college{4pB8bLUlFGrGHlaAUpjpxmnvSaG.01N4IDOxwCO1gjNzEzW}        
hacker@terminal-multiplexing~finding-sessions:~$         
'''    

## What I Learnt
I learnt the use of 'screen -ls' command that shows the list of all screens in the terminal which are either attached/detached or even remote/dead.This can help us find a screen if we close it by accident.    

## References
None.       


<img width="977" height="288" alt="image" src="https://github.com/user-attachments/assets/e3cfda03-3fbb-4022-b689-6823241354ea" />       


<img width="977" height="124" alt="image" src="https://github.com/user-attachments/assets/85ac576f-1d40-4c37-85a3-0e9a5c85e584" />

