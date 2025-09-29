# the suid bit
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'chmod' command with an 's' prompt to get the desired output.     

## My Solve
**Flag:** 'pwn.college{EVnwkw27rowNj3iiT3YSjUEKB8b.QXzEjN0wCO1gjNzEzW}'    

Here,we use the 'chmod' command with 's' prompt in the terminal.'chmod u+s' commands gives the user a suid bit which stands for 'set user id permissions bit' which lets the user act as the owner of the file.Here,we are asked to create a SUID bit for the '/challenge/getroot' after which if we run the command,it successfully creates a shell wherein we have full access to the file '/flag' which holds the flag output.Hence on reading the '/flag' file using 'cat' command,we get the final output.     
'''     
Connected!                                                                            
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot    
hacker@permissions~the-suid-bit:~$ /challenge/getroot     
SUCCESS! You have set the suid bit on this program, and it is running as root!      
Here is your shell...    
root@permissions~the-suid-bit:~# cat /flag     
pwn.college{EVnwkw27rowNj3iiT3YSjUEKB8b.QXzEjN0wCO1gjNzEzW}     
root@permissions~the-suid-bit:~#       
'''      

## What I Learnt
I learnt the use of 'chmod u/g/o+s' command which creates a suid bit for a program that lets the user act as the owner of the file given as argument.    

## References 
None.     

<img width="636" height="128" alt="image" src="https://github.com/user-attachments/assets/d2a24086-cbb3-4ff2-a4a3-3f3bdd22a787" />
