# Other users with su
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'su' command to obtain the desired output.      

## My Solve
**Flag:** 'pwn.college{gxTSS8ifR-PtaxzT-oirF3z-8va.QX2UDN1wCO1gjNzEzW}'       

Here,we use the 'su' command in the terminal.By default,the 'su' command elevates user access to root level,but we can also switch to another user.In this case,we are asked to switch to zardus.Hence we do so by using 'su zardus' for which it asks for the user's password.Once we enter the password correctly it switches to zardus after which we can the '/challenge/run' command and succesfully complete the challenge,thereby getting the flag value.      

'''        
Connected!                                                                            
hacker@users~other-users-with-su:~$ su zardus      
Password:       
zardus@users~other-users-with-su:/home/hacker$ /challenge/run       
Congratulations, you have become Zardus! Here is your flag:       
pwn.college{gxTSS8ifR-PtaxzT-oirF3z-8va.QX2UDN1wCO1gjNzEzW}     
zardus@users~other-users-with-su:/home/hacker$       
'''      

## What I Learnt
I learnt the further usage of the 'su' command which can also be used to switch to other users provided we have that specific user's password.    

## References
None.       

<img width="747" height="104" alt="image" src="https://github.com/user-attachments/assets/0c8a8e44-f1d1-4c50-9b91-1cdcc65c21ec" />
