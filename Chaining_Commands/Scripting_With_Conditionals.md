# Scripting with conditionals
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'bash' command with conditional statements to get the desired output.     

## My Solve
**Flag:** 'pwn.college{8hK-Il5OxQWbBNmwNttmWuH3AiR.0lNzMDOxwCO1gjNzEzW}'      

Here,we use conditional statements in the script shell.The conditional statements are used to check if a certain condition is satisfied and then executes the command.Here we use 'if' statement to check for the condition,in this case if the argument is "pwn".Hence we use the 'if' statement and 'fi' to create a conditional loop that checks for the argument in the script shell.We also add the shebang to let linux know it is a bash script.Then we save it under 'solve.sh' and run it using the 'bash' command.We see that for 'pwn' arugment it prints college and doesn’t print anything if the argument is different.Once successfully done,we run '/challenge/run' which checks for the script and then gives us the flag value.    
'''      
Connected!                                                                              
hacker@chaining~scripting-with-conditionals:~$ bash /home/hacker/solve.sh "pwn"        
college        
hacker@chaining~scripting-with-conditionals:~$ bash /home/hacker/solve.sh "pwnn"        
hacker@chaining~scripting-with-conditionals:~$ /challenge/run        
Correct! Your script properly handles all the conditions.      
Here's your flag:      
pwn.college{8hK-Il5OxQWbBNmwNttmWuH3AiR.0lNzMDOxwCO1gjNzEzW}      
hacker@chaining~scripting-with-conditionals:~$       
'''     

## What I Learnt 
I learnt the use of conditionals which involve checking for a condition and executing a command only if the condition is satisifed.This is done in the script shell using shebangs and 'if' statement.     

## References
None.       


<img width="601" height="138" alt="image" src="https://github.com/user-attachments/assets/437de3d2-77f7-4d7d-9183-fcafd863835d" />    



<img width="1070" height="584" alt="image" src="https://github.com/user-attachments/assets/15c52e93-b313-490f-84aa-7f4887e3768d" />
