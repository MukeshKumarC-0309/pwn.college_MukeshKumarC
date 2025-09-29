# Starting Background Processes
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '&' command to get the desired output.         

## My Solve
**Flag:** 'pwn.college{szocl3FcCF7UpfuLaG447jZjGIn.QX5QDO0wCO1gjNzEzW}'       

Here,we use the '&' command in the terminal.The '&' command is used to run a certain processes in the background which is passed as the argument.Here,we are asked to run '/challenge/run' in the background.So,if we run '/challenge/run &',our challenge is completed and we get the flag output.       
'''        
Connected!                                                                           
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &       
[1] 162           
hacker@processes~starting-backgrounded-processes:~$            
             
           
Yay, you started me in the background! Because of that, this text will probably           
overlap weirdly with the shell prompt, but you're used to that by now...        
        
Anyways! Here is your flag!         
pwn.college{szocl3FcCF7UpfuLaG447jZjGIn.QX5QDO0wCO1gjNzEzW}        
       
[1]+  Done                    /challenge/run        
hacker@processes~starting-backgrounded-processes:~$        
'''      

## What I Learnt
I learnt the use of '&' command which is used to run a specific process in the background which is mentioned in argument.     

## References
None.          


<img width="747" height="200" alt="image" src="https://github.com/user-attachments/assets/0b6e2f48-4119-4748-b30a-91d69a821d69" />
