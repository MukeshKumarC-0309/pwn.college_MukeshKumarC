# Executable Files 
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'chmod' command to get the desired output.      

## My Solve
**Flag:** 'pwn.college{40hkW2IB42Jt27H5IethHbLuCIi.QXyEjN0wCO1gjNzEzW}'     

Here,we use the 'chmod' command in the terminal.The 'chmod' command is used to change file permissions for different users according the arugments given.Here we are asked to run the file '/challenge/run'.Hence we first use 'ls -l' command to find out the permissions.We see that the user is 'hacker' ie.us and user does not have exceute permissions.Hence we use 'chmod u+x /challenge/run' to add execute permissions for the user.After this we can run the '/challenge/run' command succesfully and get the flag output.      
'''      
Connected!                                                                               
hacker@permissions~executable-files:~$ ls -l /challenge/run       
-r--r--r-- 1 hacker hacker 32 Jan 14  2025 /challenge/run        
hacker@permissions~executable-files:~$ chmod u+x /challenge/run         
hacker@permissions~executable-files:~$ /challenge/run          
Successful execution! Here is your flag:                     
pwn.college{40hkW2IB42Jt27H5IethHbLuCIi.QXyEjN0wCO1gjNzEzW}          
hacker@permissions~executable-files:~$          
'''        

## What I learnt
I learnt the use of 'chmod' command which can be used to give file permissions to different users including the permission to execute files/commands.        

## References
None.         


<img width="747" height="133" alt="image" src="https://github.com/user-attachments/assets/790b1d26-6a5b-4b04-b59b-e88141a5e173" />
