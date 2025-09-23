# Implicit Relative Path
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the './' commands to implicitly specify relative file paths to get desired result.    
## My Solve
**Flag:** 'pwn.college{M7UjpoGkSxJlwyYMHzx3OUfyiJx.QXxUTN0wCO1gjNzEzW}'   

Here,as specified we switch to the '/challenge' directory as it holds the required file.We do so by using the 'cd' command to change directories.Next we use the './run' command to implicitly specify the file path so that it could be run thereby giving us the required flag.  

'''   
hacker@paths~implicit-relative-path:~$ cd /challenge    
hacker@paths~implicit-relative-path:/challenge$ ./run     
Correct!!!     
./run is a relative path, invoked from the right directory!     
Here is your flag:     
pwn.college{M7UjpoGkSxJlwyYMHzx3OUfyiJx.QXxUTN0wCO1gjNzEzW}       
hacker@paths~implicit-relative-path:/challenge$       
'''   

## What I learnt
I learnt that by using the './' command we can implicitly mention relative file paths and can overcome limitation presented by directly running the file.   

## References
None.    

<img width="691" height="108" alt="image" src="https://github.com/user-attachments/assets/601677e1-cb44-4cac-b2af-0a1f2cefbc1b" />

