# Redirecting Output
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'echo' command along with '>' to get the desired output.       

## My Solve
**Flag:** 'pwn.college{oOYO-K5C5ctm2nWH_H9TuW3aSvE.QX0YTN0wCO1gjNzEzW}'      

Here,we are asked to use the echo command in the terminal.The 'echo' comand is used to print the arguements given.Here we are asked to redirect the output to a different file.Hence we can the '>' prompt that redirect the output to the next argument,which in this case is another file.Hence on giving the command 'echo PWN > COLLEGE' succefully redirects the output,giving us the flag.   
'''   
Connected!                                                                            
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE     
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your      
flag:    
pwn.college{oOYO-K5C5ctm2nWH_H9TuW3aSvE.QX0YTN0wCO1gjNzEzW}      
hacker@piping~redirecting-output:~$      
'''    

## What I Learnt
I learnt the use of '>' along with the 'echo' command which can be used redirect outputs to different files across different directories.   

## References
None.     

<img width="784" height="97" alt="image" src="https://github.com/user-attachments/assets/7be35fb0-240e-4279-bde4-4372f6a1ed37" />
