# Reading Manuals
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'man' command to obtain desired output.      
## My Solve
**Flag:** 'pwn.college{kYzGLkMtYHwL04EOnGzIGs5HWyw.QX0EDO0wCO1gjNzEzW}'   

First,we use the 'man' command in the terminal.The 'man' command gives the necessary details about the file or directory whichever is present in the arguement.here,we run the 'man' command with the 'challenge' as its arguement which prints the details of the arguement.Among them is the clue ,more specifically the '--kzktwn NUM' arugement which can be given along with the '/challenge' statement indicates that it will print the flag when the NUM is 045.Hence on passing '/challenge/challenge --kzktwn 045' in the terminal,we get the flag output.  
'''      
hacker@man~reading-manuals:~$ man challenge     
hacker@man~reading-manuals:~$ /challenge/challenge  --kzktwn 045     
Correct usage! Your flag: pwn.college{kYzGLkMtYHwL04EOnGzIGs5HWyw.QX0EDO0wCO1gjNzEzW}      
hacker@man~reading-manuals:~$     
'''    

## What I Learnt
I learnt the use of 'man' command(in short for manual) which prints the manual of the command given as arguement which can help us learn more abt a certain command.  

## References
None.

<img width="601" height="59" alt="image" src="https://github.com/user-attachments/assets/d94b7d02-ddb6-4380-b6b4-ac72d996e526" />

