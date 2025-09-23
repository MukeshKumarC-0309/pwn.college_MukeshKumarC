# Cat,not the pet but the command  
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'cat' command with an arguement to get the desired file
## My Solve
**Flag:** 'pwn.college{EC5RUfuPX4542DEwZrLJOxbbpF5.QXxcTN0wCO1gjNzEzW}'   

First,we exceute the 'cat' command in the terminal.Cat command is used to read the files which are stored in the directory.Cat,followed by the file name as arguement can be used to read files.Here,the arguement is the file 'flag' which when used with the cat command gives us the flag.   

'''  
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag    
pwn.college{EC5RUfuPX4542DEwZrLJOxbbpF5.QXxcTN0wCO1gjNzEzW}      
hacker@commands~cat-not-the-pet-but-the-command:~$      
'''   

## What I learnt
I learnt the use of the 'cat' command which can be used to read the files,given as the arguement.  

## References
None.

<img width="540" height="54" alt="image" src="https://github.com/user-attachments/assets/7e3e6aca-86da-4720-a0c4-b9290e069962" />
