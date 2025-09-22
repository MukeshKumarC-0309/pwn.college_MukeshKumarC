# Position Thy Self
The challenge asks you to open the terminal in the pwn.college DOJO and switch to a certain directory to obtain the necessary results

## My Solve
**Flag:** 'pwn.college{g36X4s9RyxN0z6_hj2yX4jnLpp3.QX2QTN0wCO1gjNzEzW}'  

Here,we start off by running the usual '/challenge/run' command to get our flag,but this time an unexpected error occurs because the required file isn’t in the current directory.Hence the CLI instructs us to switch to the directory which does have the file,in this case the '/var' directory.Then to switch to the given directory we use the 'cd' command which is used to change into the specified directory.After changing the directory running the first command again gives us the desired flag.  

'''  
hacker@paths~position-thy-self:~$ /challenge/run  
Incorrect...  
You are not currently in the /var directory.   
Please use the `cd` utility to change directory appropriately.   
hacker@paths~position-thy-self:~$ cd /var   
hacker@paths~position-thy-self:/var$ /challenge/run   
Correct!!!    
/challenge/run is an absolute path, invoked from the right directory!   
Here is your flag:   
pwn.college{g36X4s9RyxN0z6_hj2yX4jnLpp3.QX2QTN0wCO1gjNzEzW}   
hacker@paths~position-thy-self:/var$   
'''   

## What I learnt
I learnt that sometimes our specific file might not be in the current directories and we learn the use of 'cd' command which can be used to switch between directories.  

## References
None.

<img width="753" height="163" alt="image" src="https://github.com/user-attachments/assets/5e4717be-b4c7-4943-a405-c67492b49228" />

