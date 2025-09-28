# Printing Variables
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'echo' command to obtain desired results.

## My Solve
**Flag:** 'pwn.college{YeaI_Y7uAX_sqFs0xi22S75esMy.QX3UTN0wCO1gjNzEzW}'    

Here,the flag is hidden in a variable FLAG.Hence we use the echo command to get the result.As we know,echo command is used to print whatever is given in the argument.Hence it can be used to print variables also.For variables,we need to specify a '$' before the name to indicate it's a variable.Hence on running 'echo $FLAG' we get the flag output.    
'''    
Connected!                                                                           
hacker@variables~printing-variables:~$ echo $FLAG     
pwn.college{YeaI_Y7uAX_sqFs0xi22S75esMy.QX3UTN0wCO1gjNzEzW}       
hacker@variables~printing-variables:~$        
'''     

## What I Learnt
I learnt the use of variables and on how to read them using the 'echo' command by specifying a '$' before it.    

## References
None.    


<img width="537" height="68" alt="image" src="https://github.com/user-attachments/assets/2a96f055-b236-4694-9895-65a1df54abe6" />
