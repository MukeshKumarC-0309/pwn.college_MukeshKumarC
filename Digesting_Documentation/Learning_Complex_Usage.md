# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke arguements to get desired result.     

## My Solve
**Flag:** 'pwn.college{8nA-HV7a8enxh1b8q0c2nqyRPzT.QX1ITO0wCO1gjNzEzW}'   

Here we are instructed to use the --printfile arguement which prints whichever files are given as further arguements,in this case first we run the '/challenge/challenge --printfile /challenge/DESCRIPTION.md' that reads a description of the file choosen.Following this same logic we run the same code again with '/flag' file as the command,therefore running '/challenge/challenge --printfile /flag' gives us the flag ouput.  
'''  
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/DESCRIPTION.md      
Correct argument! Here is the /challenge/DESCRIPTION.md file:      
While using most commands is straightforward, the usage of some commands can get quite complex.     
For example, the arguments to commands like `sed` and `awk`, which we're definitely not getting into right now, are entire programs in an esoteric programming language!     
Somewhere on the spectrum between `cd` and `awk` are commands that take arguments to their arguments...       

This sounds crazy, but you've already encountered this with the `find` level in [Basic Commands](/linux-luminarium/commands).     
`find` has a `-name` argument, and the `-name` argument itself takes an argument specifying the name to search for.       
Many other commands are analogous.       

Here is this level's documentation for `/challenge/challenge`:       

> Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the description of the level!        

Given that documentation, go get the flag!      
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag    
Correct argument! Here is the /flag file:     
pwn.college{8nA-HV7a8enxh1b8q0c2nqyRPzT.QX1ITO0wCO1gjNzEzW}    
hacker@man~learning-complex-usage:~$     
'''

## What I Learnt
I learnt that we can use different arguements that fulfill different commands to access certain files which are beyond our given permission.    

## References
None.


<img width="1423" height="225" alt="image" src="https://github.com/user-attachments/assets/e90136bb-2e86-40e1-a22e-df9a9ca15b08" />     


<img width="579" height="59" alt="image" src="https://github.com/user-attachments/assets/2c1002fe-41b3-4f06-988a-c77c041c32ed" />



