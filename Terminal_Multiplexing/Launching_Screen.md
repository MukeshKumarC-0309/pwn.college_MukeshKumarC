# Launching Screen
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'screen' command to get the desired output.      

## My Solve
**Flag:** 'pwn.college{4iVQPYIKuViTCCUb_CnsbFDtF2N.0VN4IDOxwCO1gjNzEzW}'    

Here,we use the 'screen' command in the terminal.screen is a program that creates virtual terminals inside your terminal. It's somewhat like having multiple browser tabs, but for your command line.To start a screen,just execute 'screen' and it will start a screen.In this challenge,they made it so that starting a screen gives us the flag,hence getting flag output successfully after exceuting 'screen'.       
'''       
Connected!                                                                          
hacker@terminal-multiplexing~launching-screen:~$ screen        
            
          
Congratulations! You're inside a screen session!      
Here's your flag:      
pwn.college{4iVQPYIKuViTCCUb_CnsbFDtF2N.0VN4IDOxwCO1gjNzEzW}      
hacker@terminal-multiplexing~launching-screen:~$         
'''      

## What I Learnt 
I learnt the use of 'screen' command which creates a screen,similar to virtual terminals inside a terminal.     

## References
None.      


<img width="508" height="120" alt="image" src="https://github.com/user-attachments/assets/3b084925-5ab8-418a-b139-2c6ccb97a3c6" />     



<img width="508" height="81" alt="image" src="https://github.com/user-attachments/assets/a9893380-5b6a-46cc-9478-831fab1cd525" />
