# Home Sweet Home
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '~' prompt as arguement to running the '/challenge/run' command.    
## My Solve
**Flag:** 'pwn.college{sX8SdRsYVgShcp1ahpNMHr5Y2P9.QXzMDO0wCO1gjNzEzW}'    

Here we are instructed to run the 'challenge/run' command with any file path as its arguement to copy the file there,but when we give the full file path here(ie./home/hacker) it shows an unexpected error stating that the arguements must not be more than 3 characters long.That's when we realise that we can use the '~' prompt which stands for the current working directory in this case '/home/hackers'.Hence we replace the arguement by '~/~' which stands for '/home/hackers/~' as the present arguement,we get no errors and the file is succesfully copied and simultaneousy it also shows us the flag.  

'''    
hacker@paths~home-sweet-home:~$ /challenge/run /home/hacker    
The argument you provided must not have been longer than 3 characters (it's        
currently 12 characters long)!       
hacker@paths~home-sweet-home:~$ /challenge/run ~/~            
Writing the file to /home/hacker/~!       
... and reading it back to you:       
pwn.college{sX8SdRsYVgShcp1ahpNMHr5Y2P9.QXzMDO0wCO1gjNzEzW}       
hacker@paths~home-sweet-home:~$       
'''      

## What I learnt
I learnt that when we need to specify a longer file path as an argument,we can shorten them by using the '~' prompt which stands for the current working directory.    

## References
None.     


<img width="540" height="119" alt="image" src="https://github.com/user-attachments/assets/1919e48e-7f55-4122-8fe2-5ce98f0b0d71" />


