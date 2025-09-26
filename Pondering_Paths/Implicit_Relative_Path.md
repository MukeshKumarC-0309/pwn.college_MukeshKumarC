# Implicit Relative Path
The challenge asks you to open the terminal in the pwn.college DOJO and use relative path to get to the desired output using 'pwd' and '/' commands.      

## My Solve
**Flag:** 'pwn.college{YS9B-MJABju9qAkRwrmzQd-Gxzf.QX5QTN0wCO1gjNzEzW}'     

First we switch to the '/' directory as mentioned by the challenge and since we are supposed to use the relative path,i use the 'ls' command to see the list of files/directories present.Among them,challenge is the right directory as the clue said it starts with a c,hence i use 'challenge/run' command(relative file path) to get the desired output.It also works with no errors and gives the desired flag.  

'''  
hacker@paths~implicit-relative-paths-from-:~$ cd /  
hacker@paths~implicit-relative-paths-from-:/$ ls   
bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var   
hacker@paths~implicit-relative-paths-from-:/$ challenge/run    
Correct!!!        
challenge/run is a relative path, invoked from the right directory!    
Here is your flag:      
pwn.college{YS9B-MJABju9qAkRwrmzQd-Gxzf.QX5QTN0wCO1gjNzEzW}    
hacker@paths~implicit-relative-paths-from-:/$     
'''   

## What I learnt
I learnt that we can also use relative paths to get to the desired files which just involves the original path without the first '/'.Hence we can also learn to use relative file paths to navigate between directories and access the files.  

## References
None.    

<img width="985" height="133" alt="image" src="https://github.com/user-attachments/assets/716ce23f-d616-47f5-bef7-dd8520681c2b" />




