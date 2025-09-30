# Scripting with arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'bash' and 'echo' command to get the desired output.     

## My Solve
**Flag:** 'pwn.college{Ah-fMb6IGNgVLuqTRXmdVJWbI3C.0VNzMDOxwCO1gjNzEzW}'      

Here,we are asked to reverse 2 arguments given by the user in the terminal inside a script shell.Hence,we create the shebang for a bash shell and type in 'echo "$2" "$1"' which will reverse print the arguments given by the user.Then,we save it under 'solve.sh' and run it using the 'bash' command with the arguments as "hello" and "world".The script works and reverse prints them.Next we run the '/challenge/run' command which checks if the script is correct and then gives the flag value.     
'''     
Connected!                                                                            
hacker@chaining~scripting-with-arguments:~$ bash /home/hacker/solve.sh pwn college      
college pwn      
hacker@chaining~scripting-with-arguments:~$ /challenge/run    
Correct! Your script properly reversed the arguments.    
Here's your flag:      
pwn.college{Ah-fMb6IGNgVLuqTRXmdVJWbI3C.0VNzMDOxwCO1gjNzEzW}      
hacker@chaining~scripting-with-arguments:~$       
'''     

## What I Learnt 
I learnt that we can also run scripts with arguments given in the terminal which the script uses to give the correct output.     

## References
None.     

<img width="597" height="129" alt="image" src="https://github.com/user-attachments/assets/ef4ccc9f-6922-4352-9134-145545434d0e" />    


<img width="1070" height="584" alt="image" src="https://github.com/user-attachments/assets/7e1a49c5-6ebc-4707-a5f9-5dca6455ad18" />

