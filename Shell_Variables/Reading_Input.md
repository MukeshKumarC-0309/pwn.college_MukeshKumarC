# Reading Input
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'read' command to get the desired output.    

## My Solve
**Flag:** 'pwn.college{QnXKPNr0cB2jR1HOvD-7isQsVgc.QX4cTN0wCO1gjNzEzW}'     

Here,we are asked to store the value 'COLLEGE' to the variable 'PWN' but it has to be entered by the user.Hence,the 'read' commands becomes useful here.The 'read' command is used to get input from the user.Since we have to save the value in the variable 'PWN',the code would be 'read -p "INPUT:" PWN' where the phrase under double quotes is the message it will print that prompts the user to input the value and then the variable name is given as argument.On running that,it prints "INPUT:" and asks us to give the input.On giving 'COLLEGE' as the input,we succesfully complete the challenge and it provides us with the flag output.    
'''   
Connected!                                                                              
hacker@variables~reading-input:~$ read -p "INPUT:" PWN      
INPUT:COLLEGE      
You've set the PWN variable properly! As promised, here is the flag:     
pwn.college{QnXKPNr0cB2jR1HOvD-7isQsVgc.QX4cTN0wCO1gjNzEzW}     
hacker@variables~reading-input:~$      
'''     

## What I Learnt
I learnt the use of 'read' command which lets the user input the value to variables which can be used later in the shell.   

## References
None.    

<img width="724" height="102" alt="image" src="https://github.com/user-attachments/assets/64e28749-d3c0-42aa-af79-a72b3dc95cbe" />


