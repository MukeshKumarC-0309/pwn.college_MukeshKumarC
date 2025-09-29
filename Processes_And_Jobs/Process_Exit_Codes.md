# Process Exit Codes
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'echo $?' to get the desired output.     

## My Solve
**Flag:** 'pwn.college{gs0GNz5OzoR1KvF970FinjvydZ0.QX5YDO1wCO1gjNzEzW}'       

Here,we use the 'echo $?' command in the terminal.The 'echo $?' is used to deliver the exit codes in the terminal.The exit codes let us know if the command was run succesfully or not.'0' indicates it was run successfully and if it shows any other number,it indicates an error.Here,we are asked '/challenge/get-code' which exits with an exit code.We can get the exit code by using 'echo $?' which gives us a value.Using that value as the argument,we run '/challenge/submit-code' which completes the challenge giving us the flag output.    
'''        
Connected!                                                                         
hacker@processes~process-exit-codes:~$ /challenge/get-code          
Exiting with an error code!      
hacker@processes~process-exit-codes:~$ echo $?       
40        
hacker@processes~process-exit-codes:~$ /challenge/submit-code 40         
CORRECT! Here is your flag:      
pwn.college{gs0GNz5OzoR1KvF970FinjvydZ0.QX5YDO1wCO1gjNzEzW}          
hacker@processes~process-exit-codes:~$       
'''     

## What I Learnt
I learnt the use of 'echo $?' command which shows us the exit code which can help us identify if a command was run successfully or not.        

## References
None.           


<img width="747" height="136" alt="image" src="https://github.com/user-attachments/assets/9fbfe2a4-b051-473e-864a-3b2665051e86" />
