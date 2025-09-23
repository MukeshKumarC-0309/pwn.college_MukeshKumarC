# Moving Files
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'mv' command to move the file's location to get the desired output.    

## My Solve
**Flag:** 'pwn.college{8V3l6F9DiKmEA0404OEWytkjea5.0VOxEzNxwCO1gjNzEzW}'      

Here,we use the 'mv' command in the terminal.The 'mv' command is used to move files around.Here,we have been instructed to move the '/flag' to '/tmp/hack-the-planet'.Hence by doing so we get a confirmation message that the files has been moved.After that,upon running the '/challenge/check' command we get the desired output.  
'''   
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet    
Correct! Performing 'mv /flag /tmp/hack-the-planet'.    
hacker@commands~moving-files:~$ /challenge/check    
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:    
pwn.college{8V3l6F9DiKmEA0404OEWytkjea5.0VOxEzNxwCO1gjNzEzW}      

hacker@commands~moving-files:~$     
'''   

## What I learnt
I learnt the use of 'mv' command and its syntax.The 'mv' command can be used to move files around in the directories by specifying the old and new location(file path).    

## References
None.   


<img width="654" height="102" alt="image" src="https://github.com/user-attachments/assets/46e22e1c-88f6-42e0-b125-df050bbf3aa6" />
