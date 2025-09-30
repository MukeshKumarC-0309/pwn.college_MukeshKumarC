# Scripting_With_Default_Cases
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'bash' command along with conditionals to get the desired output.      

## My Solve
**Flag:** 'pwn.college{oC9QvQ6xY-9S6aKrgj9hWndcki-.01NzMDOxwCO1gjNzEzW}'     

Here,we use 'if-else' statement as a conditional in the shell script.The 'if-else' condition works in a way wherein if the given condition is satisfied a certain command is executed and if not,a different command is exceuted.In this case it’s given if the argument is 'pwn' print 'college' otherwise print 'nope'.Hence we use the 'if-else' statement with the 'fi' statement to create a loop which checks for the condition in the file editor.After saving it,if we run it in the terminal using the 'bash' command,we see that if 'pwn' is the argument,it prints 'college' and if the argument is different,it prints 'nope'.Hence after successfully completing it,we run the '/challenge/run' which checks for the scripts and then gives us the flag value.      
'''     
Connected!                                                                            
hacker@chaining~scripting-with-default-cases:~$ bash /home/hacker/solve.sh "pwn"    
college    
hacker@chaining~scripting-with-default-cases:~$ bash /home/hacker/solve.sh "pwnn"    
nope    
hacker@chaining~scripting-with-default-cases:~$ /challenge/run    
Correct! Your script properly handles the if/else conditions.    
Here's your flag:      
pwn.college{oC9QvQ6xY-9S6aKrgj9hWndcki-.01NzMDOxwCO1gjNzEzW}      
hacker@chaining~scripting-with-default-cases:~$         
'''     

## What I Learnt
I learnt the use of 'if-else' conditional statement in which if the condition is satisfied a certain command is executed and if not,there's a default case under 'else' which gets exceuted.     

## References
None.      

<img width="601" height="146" alt="image" src="https://github.com/user-attachments/assets/d65843c2-ae77-4c8f-a3ee-ec62c5b1e85c" />     


<img width="1073" height="582" alt="image" src="https://github.com/user-attachments/assets/eb25014c-5c65-4933-bcb7-89837a2788f0" />

