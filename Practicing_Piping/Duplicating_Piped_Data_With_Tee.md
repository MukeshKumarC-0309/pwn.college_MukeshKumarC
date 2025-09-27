# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'tee' commands to obtain the desired output.   

## My Solve
**Flag:** 'pwn.college{spAGSRzp1lyNMTcn_MdcOfIDPiZ.QXxITO0wCO1gjNzEzW}'      

Here,we are asked to pipe '/challenge/pwn' to '/challenge/college' but we need to intercept the data in between to find what need to give along with '/challenge/pwn'.Hence we create a tee which is basically a duplicated pipe in between to find out the data.On putting '/challenge/pwn | tee code | /challenge/college',we get a error saying that the correct code wasn’t provided to the /college part and terminates,indicating that the data has been transferred off to 'code'.So on opening 'code' using the cat command,we find that along with '/challenge/pwn' we need to add a '--secret' argument with a code,which in this case was "spAGSRzp".Hence our final command,being '/challenge/pwn --secret "spAGSRzp" | tee | /challenge/college' when run completes it successfully and we get the flag value.      
'''     
Connected!                                                                             
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee code | /challenge/college      
Processing...     
The input to 'college' does not contain the correct secret code! This code    
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the      
output of 'pwn' and figure out what the code needs to be.     
hacker@piping~duplicating-piped-data-with-tee:~$ cat code     
Usage: /challenge/pwn --secret [SECRET_ARG]     
     
SECRET_ARG should be "spAGSRzp"     
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret "spAGSRzp" | tee | /challenge/college      
Processing...      
Correct! Passing secret value to /challenge/college...     
Great job! Here is your flag:     
pwn.college{spAGSRzp1lyNMTcn_MdcOfIDPiZ.QXxITO0wCO1gjNzEzW}    
hacker@piping~duplicating-piped-data-with-tee:~$      
'''   

## What I Learnt
I learnt the use of 'tee' which is basically like a duplicate pipe used to duplicate data for 'n' number of times which can be used to read data in between.    

## References
None.   

<img width="676" height="42" alt="image" src="https://github.com/user-attachments/assets/297596a6-e3e2-43f3-aed6-54df12a20513" />     


<img width="788" height="194" alt="image" src="https://github.com/user-attachments/assets/ac10b4b1-1f72-49f9-9c9f-11a88f3f4642" />

