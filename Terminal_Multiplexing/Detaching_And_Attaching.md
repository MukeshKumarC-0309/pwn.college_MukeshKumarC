# Detaching and attaching
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'screen' command and some prompts to get the desired result.      

## My Solve
**Flag:** 'pwn.college{s8ch8R03SA3MQXfsAqQLHxILXll.0lN4IDOxwCO1gjNzEzW}'      

Here,we are asked to create a screen,detach it,run '/challenge/run' and reattach the screen.Hence,we start by loading a screen using the 'screen' command.To deatch a screen,we need to use control+a and then press d to detach it.Once done,it shows a message stating the screen has been detached.Then we run the '/challenge/run' command for which it checks for the detached screen and sends to the flag to it.Then we can reattach the screen by using 'screen -r' command after which it displays the flag which had been sent before.     
'''       
Connected!                                                                        
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen        
[detached from 162.pts-0.terminal-multiplexing~detaching-and-attaching]        
hacker@terminal-multiplexing~detaching-and-attaching:~$ /challenge/run        
Found detached screen session: 162.pts-0.terminal-multiplexing~detaching-and-attaching        
Sending flag to your screen session...        
        
Flag sent! Now reattach to your screen session with:        
          
  screen -r          
          
You'll find the flag waiting for you there!          
hacker@terminal-multiplexing~detaching-and-attaching:~$ screen -r          
        
        
        
        
hacker@terminal-multiplexing~detaching-and-attaching:~$ echo Yes! Flag is: pwn.college{s8ch8R03SA3MQXfsAqQLHxILXll.0lN4IDOxwCO1gjNzEzW}          
Yes! Flag is: pwn.college{s8ch8R03SA3MQXfsAqQLHxILXll.0lN4IDOxwCO1gjNzEzW}      
hacker@terminal-multiplexing~detaching-and-attaching:~$       
'''     

## What I Learnt
I learnt the use of control+a and d which are used to detach a screen from the terminal and the use of 'screen -r' to reattach the screen.      

## References
None.       

<img width="706" height="321" alt="image" src="https://github.com/user-attachments/assets/1e497f39-0a54-46ff-a1df-fb333df612c8" />         


<img width="990" height="143" alt="image" src="https://github.com/user-attachments/assets/995c2e6f-8671-4e24-b5b0-bc0b09adf0c0" />

