# Position Elsewhere
The challenge asks you to open the terminal in the pwn.college DOJO and use the 'cd' command to change to the specific directory and then specify the file path to get the desired result   

## My Solve
**Flag:** 'pwn.college{0GLj1_vIjXlHMpWTXTXnmyyXhOl.QX3QTN0wCO1gjNzEzW}'   

We start by using the '/challenge/run' command to access our flag but we have an unexpected error which indicates that the choosen file is not present in the current directory.It says that the file is there in the /usr/share/doc directory.So,next we use 'cd /usr/share/doc' command to switch to said directory.After that,on rerunning the first command,we get no errors and we get the desired result(flag).  

'''  
hacker@paths~position-elsewhere:~$ /challenge/run  
Incorrect...   
You are not currently in the /usr/share/doc directory.    
Please use the `cd` utility to change directory appropriately.   
hacker@paths~position-elsewhere:~$ cd /usr/share/doc   
hacker@paths~position-elsewhere:/usr/share/doc$ /challenge/run   
Correct!!!   
/challenge/run is an absolute path, invoked from the right directory!   
Here is your flag:   
pwn.college{0GLj1_vIjXlHMpWTXTXnmyyXhOl.QX3QTN0wCO1gjNzEzW}   
hacker@paths~position-elsewhere:/usr/share/doc$    
'''   

## What I learnt
I learnt the advanced use of 'cd' command in which an extended file path was given as arguement instead of a single arguement hence proving that the 'cd' command can also accept extended file paths.  

## References
None  

<img width="753" height="163" alt="image" src="https://github.com/user-attachments/assets/506048bc-779a-427e-9cca-6b12f8a2344e" />


