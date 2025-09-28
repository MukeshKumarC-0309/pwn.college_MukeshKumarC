# Split piping stderr and stdout
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the piping command and process substitution  command to get the desired output.     

## My Solve
**Flag:** 'pwn.college{4yDtP7bZBQdNBvFjImLYxZrkuSG.QXxQDM2wCO1gjNzEzW}'    

Here,we are asked to redirect the stderr and stdout of a file to 2 different locations.Hence we can use process substitution to achieve this.We start by linking the stderr part of '/challenge/hack' to '/challenge/the' by placing '2>' which stands for std err and we connect it to '/challenge/the' using '>' command which distributes the output to the specified file,and for stdout it’s pretty straightforward.We use '>' for stdout and '>(/challenge/planet)' to shift the stdout.Hence our final code '/challenge/hack 2> >(/challenge/the) > >(/challenge/planet)' when run gives us the final output.   
'''      
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) > >(/challenge/planet)     
Congratulations, you have learned a redirection technique that even experts    
struggle with! Here is your flag:    
pwn.college{4yDtP7bZBQdNBvFjImLYxZrkuSG.QXxQDM2wCO1gjNzEzW}     
hacker@piping~split-piping-stderr-and-stdout:~$      
'''     

## What I Learnt
I learnt the use of split piping to send 2 parts of a file to 2 different location using piping and prcoess substitution,denoted by '>()'.    

## References
None.    

<img width="802" height="89" alt="image" src="https://github.com/user-attachments/assets/6aaba5fb-a535-4d81-ab03-4bf787a3b51d" />
