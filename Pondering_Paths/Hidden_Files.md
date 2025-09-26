# Hidden Files 
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'ls' command along with -a prompt to get the desired output.  

## My Solve
**Flag:** 'pwn.college{4XxWaV3TDsXyaJ02OGYshYcLVKt.QXwUDO0wCO1gjNzEzW}'  

Here,we try to access the 'flag' file from the '/' directory.But we find no such file.So we use the 'ls -a' command to see all files.'ls -a' command is used to see all the files in the directory,even the hidden ones.There,we find the 'flag' file hidden in the directory.Then we use the 'cat' command to read the file,thereby getting our flag.  
'''   
hacker@commands~hidden-files:~$ cd /    
hacker@commands~hidden-files:/$ ls -a    
.           .flag-3125574024311  challenge  home   lib64   mnt  proc  sbin  tmp     
..          bin                  dev        lib    libx32  nix  root  srv   usr     
.dockerenv  boot                 etc        lib32  media   opt  run   sys   var     
hacker@commands~hidden-files:/$ cat /.flag-3125574024311     
pwn.college{4XxWaV3TDsXyaJ02OGYshYcLVKt.QXwUDO0wCO1gjNzEzW}     
hacker@commands~hidden-files:/$     
'''   

## What I learnt
I learnt the use of the '-a' prompt along with the 'ls' command to view all the files,even the ones which are hidden which is very useful if we have to search for files that aren’t visible in the directories.  

## References
None.   

<img width="654" height="118" alt="image" src="https://github.com/user-attachments/assets/2cfa0c9a-1d66-4af5-8ec2-a468af4f5753" />
