# Making Directories
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'mkdir' and 'touch' commands to obtain desired results.     

## My Solve
**Flag:** 'pwn.college{AXwl9uclGBp-GkUH3IjvUtPuQBL.QXxMDO0wCO1gjNzEzW}'       

Here,we use the 'mkdir' command in the terminal.The 'mkdir' command is used to create a new directory which in this case is the '/tmp/pwn' directory.Next,we use the 'touch' command which is used to create new file which in this case is the 'college' file.After successfully completing both steps,we run the '/challenge/run' command which gives us the flag value.  
'''    
hacker@commands~making-directories:~$ mkdir /tmp/pwn      
hacker@commands~making-directories:~$ cd /tmp/pwn      
hacker@commands~making-directories:/tmp/pwn$ touch college     
hacker@commands~making-directories:/tmp/pwn$ /challenge/run     
Success! Here is your flag:     
pwn.college{AXwl9uclGBp-GkUH3IjvUtPuQBL.QXxMDO0wCO1gjNzEzW}     
hacker@commands~making-directories:/tmp/pwn$     
'''       

## What I Learnt
I learnt the 'mkdir' command which is used to create new directories which takes the directory name as its arguement.We also learn the use of 'touch' command ie.to create new files.    

## References
None.    

<img width="626" height="113" alt="image" src="https://github.com/user-attachments/assets/49282beb-0fc9-4878-973e-f417f346708f" />
