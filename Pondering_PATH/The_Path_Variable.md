# The path variable
The challenge asks you to open the terminal in the pwn.college DOJO and manipulate the PATH variable to get the desired result.    

## My Solve
**Flag:** 'pwn.college{sx5K7KODCxm1dHI3vuhkwf5WHoy.QX2cDM1wCO1gjNzEzW}'      

Here,we are asked to run the '/challenge/run' which will delete on its own unless we manipulate the rm command.So we have to manipulate the PATH variable which contains the necessary information for the rm command.Hence we use 'export PATH=""' to disrupt the path variable and use '&&' to connect the second command which is '/challenge/run'.Hence the path variable is disrupted,there is no such command as such as rm,hence safely retrieving the flag.    
'''      
Connected!                                                                          
hacker@path~the-path-variable:~$ export PATH="" && /challenge/run        
Trying to remove /flag...        
/challenge/run: line 4: rm: No such file or directory        
The flag is still there! I might as well give it to you!      
pwn.college{sx5K7KODCxm1dHI3vuhkwf5WHoy.QX2cDM1wCO1gjNzEzW}        
hacker@path~the-path-variable:~$         
'''      

## What I Leant 
I learnt about the manipulation of the PATH variable which can be used to render certain commands useless by removing the necessary information for that command to be executed.     

## References 
None.        


Connected!                                                                        
hacker@path~the-path-variable:~$ export PATH="" && /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{sx5K7KODCxm1dHI3vuhkwf5WHoy.QX2cDM1wCO1gjNzEzW}
hacker@path~the-path-variable:~$ 
