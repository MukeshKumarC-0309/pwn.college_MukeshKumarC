# Switching Windows(Tmux)
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'tmux' commands to obtain the desired result.     

## My Solve
**Flag:** 'pwn.college{s6o10j0ogXfUKULtMhRiI4OBZ5Z.0FM5IDOxwCO1gjNzEzW}'       

Here,we are asked to switch between windows in tmux.Similar to screens,even certain commands in tmux allow us to switch between different windows,in this case using control+b and a suitable argument for a particular window.Here,we are asked to first reattach the window which we do so using 'tmux a' command,which takes us to window 1 which contains a welcome message in which it was specified we have to switch to window 0 in order to get the flag.So we use control+b followed by 0,which switches to window 0 which holds our flag thereby displaying it promptly.      
'''     
Connected!                                                                        
hacker@terminal-multiplexing~switching-windows-tmux:~$ tmux a        
            
            
          
          
        
        
          
            
 cat <<MSG            
Welcome to the tmux window switching challenge!        
You are currently in window 1.        
The flag is hidden in window 0.        
Use Ctrl-B 0 to switch to window 0!        
MSG        
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG        
> Welcome to the tmux window switching challenge!          
> You are currently in window 1.        
> The flag is hidden in window 0.        
> Use Ctrl-B 0 to switch to window 0!        
> MSG        
Welcome to the tmux window switching challenge!        
You are currently in window 1.        
The flag is hidden in window 0.        
Use Ctrl-B 0 to switch to window 0!        
hacker@terminal-multiplexing~switching-windows-tmux:~$         
            
          
          
          
          
          
            
            
          
hacker@terminal-multiplexing~switching-windows-tmux:~$  cat <<MSG        
> Excellent work! You found window 0!        
> Here is your flag: pwn.college{s6o10j0ogXfUKULtMhRiI4OBZ5Z.0FM5IDOxwCO1gjNzEzW}        
> MSG        
Excellent work! You found window 0!        
Here is your flag: pwn.college{s6o10j0ogXfUKULtMhRiI4OBZ5Z.0FM5IDOxwCO1gjNzEzW}        
hacker@terminal-multiplexing~switching-windows-tmux:~$
'''     

## What I Learnt
I learnt how to switch between multiple windows in tmux which is helpful when we are dealing with multiple windows each with their own purpose,using control+b and a suitable argument depending on which window the user wants to switch to.       

## References
None.         


<img width="785" height="269" alt="Screenshot 2025-09-30 at 1 18 04 PM" src="https://github.com/user-attachments/assets/f75457dd-77d5-4656-9c62-f01a035647d8" />      



<img width="785" height="269" alt="Screenshot 2025-09-30 at 1 17 44 PM" src="https://github.com/user-attachments/assets/23348ed8-abe8-482b-bd80-baf8f9b68b9f" />     



<img width="750" height="126" alt="Screenshot 2025-09-30 at 1 18 19 PM" src="https://github.com/user-attachments/assets/c66555b1-a9da-47f8-93d0-6e6b2e56b092" />


