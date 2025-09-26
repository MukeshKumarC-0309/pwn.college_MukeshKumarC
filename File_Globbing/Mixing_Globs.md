# Mixing Globs
The challenge asks you to open the terminal in the pwn.college DOJO and invoke different globbing techniques together to obtain desired output.    

## My Solve
**Flag:** 'pwn.college{wZ8S-tqybrOO-r0sPWKIz8BPMep.QX1IDO0wCO1gjNzEzW}'     

Here,we need to run the '/challenge/run' command with an argument that searches for 3 different files together(challenging,educational and pwning).Hence we make use of the '*' and '[]'globbing to make sure that the files start with either c or e or p by placing the argument as [cep]*.Hence we run the command as '/challenge/run [cep]*' which gives us the final output.    
'''   
Connected!                                                                            
hacker@globbing~mixing-globs:~$ cd /challenge/files    
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*     
You got it! Here is your flag!     
pwn.college{wZ8S-tqybrOO-r0sPWKIz8BPMep.QX1IDO0wCO1gjNzEzW}     
hacker@globbing~mixing-globs:/challenge/files$      
'''    

## What I Learnt
I learnt the use of combining multiple globbing techniques together to enhance the process of specifying file paths in order to tackle multiple constraints.      

## References
None.    


<img width="608" height="95" alt="image" src="https://github.com/user-attachments/assets/52fbfbcf-bcf1-4693-9371-9bc9fcbde1b0" />


