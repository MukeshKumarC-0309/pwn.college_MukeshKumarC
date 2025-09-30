# Detaching and attaching(tmux)
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'tmux' command to obtain the desired result.     

## My Solve
**Flag:** 'pwn.college{8sm2eYnUl-mT1nOSOLIRkceB2Nl.0VO4IDOxwCO1gjNzEzW}'    

Here,we are asked to use the 'tmux' comamnd in the terminal.The 'tmux' command is similar to a screen but a more modern version of it.It slightly differs from the screen in terms of certain commands,such as to detach we use control+b followed by 'd' and to attach,we use 'tmux a'.Hence according to the challenge,we have to launch a tmux,detach it,run '/challenge/run' and then reattach the tmux.Hence we start a tmux by using 'tmux',and then detach it using control+b,followed by 'd'.Then we run the '/challenge/run' for which it checks for the detached tmux and sends the flag there.Then we reattach the tmux using 'tmux a' after which the flag is displayed.      
'''       
Connected!                                                                        
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux        
[detached (from session 0)]        
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ /challenge/run      
Found detached tmux session: 0        
Sending flag to your tmux session...        
        
Flag sent! Now reattach to your tmux session with:        
  tmux attach      
          
  You'll find the flag waiting for you there!              
  hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$ tmux a        
        
        
        
        
        
        
        
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$  echo Congratulations, here is your flag: pwn.college{8sm2eYnUl-mT1nOSOLIRkceB2Nl.0VO4IDOxwCO1gjNzEzW}        
Congratulations, here is your flag: pwn.college{8sm2eYnUl-mT1nOSOLIRkceB2Nl.0VO4IDOxwCO1gjNzEzW}          
hacker@terminal-multiplexing~detaching-and-attaching-tmux:~$           
'''    

## What I Learnt
I learnt about tmux,which is a more modern,younger version of screen with much more capabilities and the commands used in tmux such as 'tmux' or 'tmux a' etc.     

## References 
None.        



<img width="862" height="407" alt="image" src="https://github.com/user-attachments/assets/834be527-5ebd-4765-ac24-fe33f42b8c06" />         



<img width="1171" height="123" alt="image" src="https://github.com/user-attachments/assets/d2436fb0-da82-46f8-ba54-be60e3c887b7" />

