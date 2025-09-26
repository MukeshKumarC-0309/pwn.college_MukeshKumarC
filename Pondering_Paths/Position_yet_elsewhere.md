# Position Thy Self
The challenge asks you to open the terminal in the pwn.college DOJO and switch to a certain directory to obtain the necessary results

## My Solve
**Flag:** 'pwn.college{EkaE9blSixmthAx1zPUYYRIq0KE.QX4QTN0wCO1gjNzEzW}'  

Here,we start off by running the usual '/challenge/run' command to get our flag,but this time an unexpected error occurs because the required file isn’t in the current directory.Hence we are instructed to switch to the directory which does have the file,in this case the '/' directory.Then to switch to the given directory we use the 'cd' command which is used to change into the specified directory.After changing the directory running the first command again gives us the desired flag.  

'''  
hacker@paths~position-thy-self:~$ /challenge/run  
Incorrect...  
You are not currently in the / directory.   
Please use the `cd` utility to change directory appropriately.   
hacker@paths~position-thy-self:~$ cd /  
hacker@paths~position-thy-self:/$ /challenge/run   
Correct!!!    
/challenge/run is an absolute path, invoked from the right directory!   
Here is your flag:   
pwn.college{EkaE9blSixmthAx1zPUYYRIq0KE.QX4QTN0wCO1gjNzEzW}     
hacker@paths~position-thy-self:/var$   
'''   

## What I learnt
I learnt that sometimes our specific file might not be in the current directories and we learn the use of 'cd' command which can be used to switch between directories.  

## References
None.   

<img width="753" height="163" alt="image" src="https://github.com/user-attachments/assets/8f665e9f-12f3-44ee-8499-9b4d4fc7c565" />


