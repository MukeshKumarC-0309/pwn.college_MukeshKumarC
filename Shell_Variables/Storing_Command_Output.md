# Storing Command Ouput
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'echo' command to get the desired result.   

## My Solve
**Flag:** 'pwn.college{A8cSCId5Hc3vIR0MjmMkc5nY6q6.QX1cDN1wCO1gjNzEzW}'     

Here,we are asked to store the output of a command in a variable.This can be done by something called as 'command substitution' which involves creation of a variable and using "$()" to store the output of the command in it.So here,we are asked to store the output of '/challenge/run' in a variable called 'PWN'.Hence,by giving "PWN=$(/challenge/run)" we successfully store the output in the variable.To run it,we just need to use the 'echo' command and run 'echo $"PWN"' and it successfully runs the program and gives us the flag output.   
'''    
Connected!                                                                             
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)     
Congratulations! You have read the flag into the PWN variable. Now print it out     
and submit it!     
hacker@variables~storing-command-output:~$ echo "$PWN"     
pwn.college{A8cSCId5Hc3vIR0MjmMkc5nY6q6.QX1cDN1wCO1gjNzEzW}      
hacker@variables~storing-command-output:~$      
'''    


## What I Learnt
I learnt the method of 'command substitution' which involves storing the output of a command in a variable using the '$()' command,which can be used later for 'n' number of times in the terminal.     

## References
None.   

<img width="833" height="116" alt="image" src="https://github.com/user-attachments/assets/5e4c8596-715c-484b-8a05-87e078458733" />


