# Chainging with semicolons
The challenge asks you to open the terminal in the pwn.college DOJO and invoke ';' to get the desired output.         

## My Solve
**Flag:** 'pwn.college{MZVfIf5mZISdIviQ68VrlpSmWb3.QX1UDO0wCO1gjNzEzW}'      

Here,we use the ';' in the terminal.The ';' is used to chain 2 or more commands together in the terminal wherein each commands happens one after another.Here we are asked to run '/challenge/pwn' and '/challenge/college' one after another.Hence we can chain them together using ';'.Our commands looks like '/challenge/pwn; /challenge/college',which completes the challenge and gives us the flag output.     
'''         
Connected!                                                                              
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn; /challenge/college          
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:        
pwn.college{MZVfIf5mZISdIviQ68VrlpSmWb3.QX1UDO0wCO1gjNzEzW}            
hacker@chaining~chaining-with-semicolons:~$            
'''     

## What I Learnt
I learnt the use of ';' which is used to chain multiple commands together so that they are executed one after another.     

## References
None.       

<img width="636" height="83" alt="image" src="https://github.com/user-attachments/assets/ab0ef404-aa87-4d28-81ec-4dadeb601fbe" />
