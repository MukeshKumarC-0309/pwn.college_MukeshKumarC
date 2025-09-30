# Finding Commands
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'which' command to obtain the desired result.      

## My Solve
**Flag:** 'pwn.college{8DCNZtSn55nwpKrFD9UqwjBY0Dh.01NzEzNxwCO1gjNzEzW}'      

Here,we are asked to find the '/flag' which is hidden in the same directory as the command 'win'.Hence we can use the 'which' command which tells us the path to a certain command.Hence 'which win' gives us the path to that command.So the directory we get is '/challenge/paths/9372/'.We use the 'cd' command to switch to that directory and then use 'ls -l' command to see the list of files and their permissions.We find the file 'flag' which can be read by us.So we use the 'cat' command to read the 'flag' file giving us the final flag value.     
'''        
Connected!                                                                              
hacker@path~finding-commands:~$ which win        
/challenge/paths/9372/win      
hacker@path~finding-commands:~$ cd /challenge/paths/9372/        
hacker@path~finding-commands:/challenge/paths/9372$ ls -l        
total 8        
-rw-r--r-- 1 root root 61 Sep 30 08:14 flag      
-rwsr-xr-x 1 root root 97 Jun  6 11:37 win        
hacker@path~finding-commands:/challenge/paths/9372$ cat flag      
pwn.college{8DCNZtSn55nwpKrFD9UqwjBY0Dh.01NzEzNxwCO1gjNzEzW}      
hacker@path~finding-commands:/challenge/paths/9372$         
'''       

## What I Learnt
I learnt the use of the 'which' command that is used to specify the file path of the command given as argument.      

## References 
None.        


<img width="750" height="181" alt="image" src="https://github.com/user-attachments/assets/12638f3a-38d5-436e-a7af-58a60fc02e64" />
