# Becoming
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'su' command to get desired output.         

## My Solve
**Flag:** 'pwn.college{cejQnUfzmCzwFnfdbEM-Fj6FLp0.QX3YTN0wCO1gjNzEzW}'        

Here,we use the 'su' command in the terminal.The 'su' command is used to elevate user access to 'root' with the password.Here,the password is 'hack-the-planet'.Hence when entered,we get root access after which we can access the flag 'myflag' using 'cat' command.Hence we complete the challenge and get the flag output.         
'''       
Connected!                                                                             
hacker@users~becoming-root-with-su:~$ su      
Password:        
root@users~becoming-root-with-su:/home/hacker# cat myflag          
      
[FLAG] Here is your flag:        
[FLAG] pwn.college{cejQnUfzmCzwFnfdbEM-Fj6FLp0.QX3YTN0wCO1gjNzEzW}      
       
root@users~becoming-root-with-su:/home/hacker#         
'''     

## What I Learnt
I learnt the use of 'sd' command which can be used to elevate user permissions to 'root' level.      

## References
None.          


<img width="747" height="133" alt="image" src="https://github.com/user-attachments/assets/93228806-4ea7-4aff-accc-40a8338d0106" />
