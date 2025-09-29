# Becoming
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'su' command to get desired output.         

## My Solve
**Flag:** 'pwn.college{cejQnUfzmCzwFnfdbEM-Fj6FLp0.QX3YTN0wCO1gjNzEzW}'        

Here,we use the 'su' command in the terminal.The 'su' command is used to elevate user access to 'root' with the password.Here,the password is 'hack-the-planet'.Hence when entered,we get root access after which we can access the flag 'myflag' using 'cat' command.Hence we complete the challenge and get the flag output.         
'''       
Connected!                                                                             
hacker@users~becoming-root-with-su:~$ su      
Password:        
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{QjC7ws-58MHMCmd3UFfutF5z5re.QX1UDN1wCO1gjNzEzW}      
root@users~becoming-root-with-su:/home/hacker#         
'''     

## What I Learnt
I learnt the use of 'sd' command which can be used to elevate user permissions to 'root' level.      

## References
None.          


<img width="747" height="94" alt="image" src="https://github.com/user-attachments/assets/32a363f7-2b20-4e99-9322-94ec5c88b341" />

