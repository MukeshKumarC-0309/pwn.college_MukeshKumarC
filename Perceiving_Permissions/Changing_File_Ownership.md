# Changing File Ownership
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'chown' command to get the desired output.     

## My Solve
**Flag:** 'pwn.college{cZJaHCHxpMU55Z7ePgXm4cKRRFp.QXxEjN0wCO1gjNzEzW}'      

Here,it’s given that we need to change the access of the '/flag' to hacker.For this we need to use the 'chown' command which is used to change ownership of a file.So here,we use 'chown hacker /flag' to change the ownership of the flag.After that we can run the '/flag' as hacker to get the output.    
'''    
Connected!                                                                              
hacker@permissions~changing-file-ownership:~$ chown hacker /flag        
hacker@permissions~changing-file-ownership:~$ cat /flag      
pwn.college{cZJaHCHxpMU55Z7ePgXm4cKRRFp.QXxEjN0wCO1gjNzEzW}         
hacker@permissions~changing-file-ownership:~$         
'''     

## What I Learnt
I learnt the use of the 'chown' command which stands for 'change ownership' is used to change the ownership of a specific file.     

## References 
None.        

<img width="747" height="81" alt="image" src="https://github.com/user-attachments/assets/1c4ada2f-f721-4396-af71-2d8b817d4ba0" />
