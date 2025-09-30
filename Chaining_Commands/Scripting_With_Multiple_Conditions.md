# Scripting With Multiple Conditions
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'bash' command and conditionals to get the desired output.     

## My Solve
**Flag:** 'pwn.college{YKxo5EjgYhw-2peSLWQa2ZGmaDF.0FOzMDOxwCO1gjNzEzW}'    

Here,we make use of the 'if-elif-else' statements.It works in the same was as 'if-else' statements but it allows for more conditions.Here,we are asked to print "the planet" if the argument is "hack",print "college" if the argument is "pwn",print "linux" if the argument is "learn" and print "unknown" if none of the condition matches.Hence we can use if for the first conditions and elif for the subsequent conditions and else for the final default case along with the 'fi' statement to create a conditional loop that checks for the argument in the file editor.Once saved,we run it in the terminal using the 'bash' command,we see that according to the arguments given it prints out different outputs("hack"="the planet","pwn"="college","learn"="linux").Hence completed,we run the '/challenge/run' which checks for the scripts and gives us the flag value.      
'''          
Connected!                                                                            
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh "hack"      
the planet        
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh "pwn"      
college      
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh "learn"      
linux        
hacker@chaining~scripting-with-multiple-conditions:~$ bash /home/hacker/solve.sh "pwnn"      
unknown        
hacker@chaining~scripting-with-multiple-conditions:~$ /challenge/run      
Correct! Your script properly handles all the conditions with elif.        
Here's your flag:        
pwn.college{YKxo5EjgYhw-2peSLWQa2ZGmaDF.0FOzMDOxwCO1gjNzEzW}      
hacker@chaining~scripting-with-multiple-conditions:~$         
'''     

## What I Learnt
I learnt the use of 'if-elif-else' statements in which we can give 2 or more options as conditions for the argument to be checked for and if none of them are satisfied,a default case which will be executed by linux.      

## References
None.    


<img width="922" height="220" alt="image" src="https://github.com/user-attachments/assets/7ea48142-1f7d-445a-97f3-2c8a754bd5ba" />     



<img width="1073" height="582" alt="image" src="https://github.com/user-attachments/assets/0d8df8e8-8d5a-4445-afa6-2f5dd4332313" />
