# Writing to multiple programs
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'tee' command and piping to get the desired output.     

## My Solve
**Flag:** 'pwn.college{ENXPtJGHnS_D5vg6YJ7SoheKMdp.QXwgDN1wCO1gjNzEzW}'    

Here,we are asked to duplicate the output of '/challenge/hack' to both '/challenge/the' and '/challenge/planet' simultaneously.To achieve this,we can make use of piping,the 'tee' command and process substitution to complete this challenge.The pipe is used to connect all the commands by using input of 1 command as the output of the other program.The 'tee' command is used to duplicate the output and process substitution is used to hook the output to a argument of commands.Hence out final code ie.'/challenge/hack | tee  >(/challenge/the)| tee >(/challenge/planet)' is successfully run and we get the final output.    
'''     
Connected!                                                                           
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee  >(/challenge/the)| tee >(/challenge/planet)     
This secret data must directly and simultaneously make it to /challenge/the and     
/challenge/planet. Don't try to copy-paste it; it changes too fast.     
8034322112545511253      
Congratulations, you have duplicated data into the input of two programs! Here      
is your flag:      
pwn.college{ENXPtJGHnS_D5vg6YJ7SoheKMdp.QXwgDN1wCO1gjNzEzW}      
hacker@piping~writing-to-multiple-programs:~$      
'''    

## What I learnt
I learnt the usage of piping,'tee' and process substitution altogether which can be used to write outputs to multiple programs.    

## References
None.    

<img width="806" height="129" alt="image" src="https://github.com/user-attachments/assets/ef2f8cfa-a7c3-4a4a-a214-3589bd2b2bc6" />
