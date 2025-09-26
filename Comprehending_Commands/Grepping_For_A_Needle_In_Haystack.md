# Grepping for needle in haystack
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'grep' command to filter out the required output.    

## My Solve
**Flag:** 'pwn.college{oqD9MeVWgeGE2_7SPFGxEOh40wU.QX3EDO0wCO1gjNzEzW}'    

Here,using the 'cat' command to read the file would be futile since it’s mentioned that the file contains thousands of lines.Hence reading though all of them would be a tiresome task.Here we can use the 'grep' command which can used to filter out certain strings from the files which have the sub-string given as arguement.Here we use the arguement as 'pwn.college' since all flags start with such strings.Doing so,we get the strings which contain the words 'pwn.college' which also gives us the desired flag.  
'''   
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt     
pwn.college{oqD9MeVWgeGE2_7SPFGxEOh40wU.QX3EDO0wCO1gjNzEzW}      
hacker@commands~grepping-for-a-needle-in-a-haystack:~$     
'''   

## What I learnt
I learnt that when we need to see only a certain part of the entire file,we can use the 'grep' command which can be used to filter out the strings that contain the arguement provided by the user.   

## References
None.   


<img width="654" height="48" alt="image" src="https://github.com/user-attachments/assets/b0ae4c46-b43b-4b42-bfec-d796054fa6ae" />
