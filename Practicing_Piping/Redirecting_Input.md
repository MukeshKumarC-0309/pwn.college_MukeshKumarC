# Redirecting Input
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '<' command to obtain desired result.   

## My Solve
**Flag:** 'pwn.college{AkgKFxyCv-prmq0v3rEzbMN7yyA.QXwcTN0wCO1gjNzEzW}'     

First we use the 'echo' command to insert the word 'COLLEGE' into the file PWN by putting 'echo COLLEGE > PWN' command using output redirection.Then we are asked to redirect the input of '/challenge/run' to PWN.This is possible by using the '<' command which can be used to redirect the input.We do so by using the command '/challenge/run < PWN' which succesfully completes the challenge giving us the flag.   
'''    
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN       
hacker@piping~redirecting-input:~$ /challenge/run < PWN     
Reading from standard input...     
Correct! You have redirected the PWN file into my standard input, and I read      
the value 'COLLEGE' out of it!     
Here is your flag:     
pwn.college{AkgKFxyCv-prmq0v3rEzbMN7yyA.QXwcTN0wCO1gjNzEzW}    
hacker@piping~redirecting-input:~$     
'''    

## What I Learnt
I learnt the use of the '<' command which can be used to redirect the input to a different location/file in addition to redirecting outputs.   

## References
None.    

<img width="654" height="122" alt="image" src="https://github.com/user-attachments/assets/72afd211-7688-4235-8936-0d23ca3c1717" />
