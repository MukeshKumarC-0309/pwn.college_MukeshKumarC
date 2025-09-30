# Switching Windows
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the control+a command to get the desired result.      

## My Solve
**Flag:** 'pwn.college{wOYk77ZvTeV2akFX_HWRyM7aMXl.0FO4IDOxwCO1gjNzEzW}'     

Here,we are asked to switch between screens.Like browsers in a web browser,when we have multiple screens we can switch between them using the control+a command and the suitable argument to switch to a particular screen.Here,we are asked to reattach the screen using 'screen -r' and on doing so,it automatically places us at window 1 which contains a welcome message and the steps to follow to switch to window 0 in this case being control+a followed by 0 to switch to window 0.Hence on doing so,we successfully switch to window 0 which contains the flag value completing the challenge.     
'''        
Connected!                                                                              
hacker@terminal-multiplexing~switching-windows:~$ screen -r      
      
      
        
        
        
      
 cat <<MSG        
Welcome to the window switching challenge!      
You are currently in window 1.      
The flag is hidden in window 0.      
Use Ctrl-A 0 to switch to window 0!      
MSG      
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG      
> Welcome to the window switching challenge!      
> You are currently in window 1.      
> The flag is hidden in window 0.      
> Use Ctrl-A 0 to switch to window 0!      
> MSG      
Welcome to the window switching challenge!      
You are currently in window 1.      
The flag is hidden in window 0.      
Use Ctrl-A 0 to switch to window 0!      
      
      
      
      
        
        
        
hacker@terminal-multiplexing~switching-windows:~$  cat <<MSG      
> Excellent work! You found window 0!        
> Here is your flag: pwn.college{wOYk77ZvTeV2akFX_HWRyM7aMXl.0FO4IDOxwCO1gjNzEzW}        
> MSG        
Excellent work! You found window 0!        
Here is your flag: pwn.college{wOYk77ZvTeV2akFX_HWRyM7aMXl.0FO4IDOxwCO1gjNzEzW}      
hacker@terminal-multiplexing~switching-windows:~$
'''

## What I Learnt
I learnt the use of control+a which can unlock options to create a new window or switch between windows according to the argument passed in the terminal.    

## References
None.         



<img width="977" height="198" alt="image" src="https://github.com/user-attachments/assets/98886aa4-4e79-429d-93df-3f579ce8b51c" />    



<img width="977" height="280" alt="image" src="https://github.com/user-attachments/assets/2e38a29b-3ff5-4724-890c-da73facc08fc" />      



<img width="862" height="91" alt="image" src="https://github.com/user-attachments/assets/1db68d8c-b404-4e0d-80e1-e52320a5878a" />


