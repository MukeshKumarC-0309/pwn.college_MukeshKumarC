# Searching Manuals  
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'man' command to get the desired output.  

## My Solve
**Flag:** 'pwn.college{w2QGOQ0vinbcoOWeGI3v82Dfub1.QX1EDO0wCO1gjNzEzW}'       

First,we use the 'man' command in the terminal.The 'man' command gives the necessary details about the file or directory whichever is present in the arguement.here,we run the 'man' command with the 'challenge' as its arguement which prints the details of the arguement(command).Among them is the clue ,more specifically the '--hrct' arugement which  can be given along with the '/challenge' statement indicates that it will print the flag.Hence on passing '/challenge/challenge --hrct' in the terminal,we get the flag output. 
'''      
hacker@man~searching-manuals:~$ man challenge     
hacker@man~searching-manuals:~$ /challenge/challenge  --hrct    
Initializing...     
Correct usage! Your flag: pwn.college{w2QGOQ0vinbcoOWeGI3v82Dfub1.QX1EDO0wCO1gjNzEzW}    
hacker@man~searching-manuals:~$        
'''    

## What I Learnt
I learnt the use of 'man' command(in short for manual) which prints the manual of the command given as arguement which can help us learn more abt a certain command.  

## References
None.    


<img width="601" height="76" alt="image" src="https://github.com/user-attachments/assets/e933175e-6168-4e0e-84b9-cdd5c0a8272b" />




