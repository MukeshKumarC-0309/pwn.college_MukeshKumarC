# Tab Completion
The challenge asks you to open the terminal in the pwn.college DOJO and use the tab command to get the desired output.     

## My Solve
**Flag:** 'pwn.college{QfvLSr6j3PG2pg4tkhYxjTPl-Yq.0FN0EzNxwCO1gjNzEzW}'       

We use the 'tab' key here in the terminal.We learn that one disadvantage of flie globbing using '*' is that it can choose the wrong file and it might be too late when we find that out.Hence a better alternative to it is to use the 'tab' button which autocompletes the command according the nearest possibilities.Hence,we run the '/challenge/pwncollege' command using tabspace to autocomplete commands to get the desired output.   

'''   
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​      
pwn.college{QfvLSr6j3PG2pg4tkhYxjTPl-Yq.0FN0EzNxwCO1gjNzEzW}     
hacker@globbing~tab-completion:~$      
'''    

## What I Learnt
I learnt the usage of the 'tab' key in the terminal ie.it helps autocomplete commands that help us saving time while writing long lines of code.    

## References
None.    

<img width="608" height="53" alt="image" src="https://github.com/user-attachments/assets/d6889e95-e73d-40ff-b710-73be1d624d65" />


