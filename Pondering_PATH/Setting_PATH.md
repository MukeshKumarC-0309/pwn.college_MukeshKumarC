# Setting Path
The challenge asks you to open the terminal in the pwn.college DOJO and manipulate the PATH variable to get the desired output.      

## My Solve
**Flag:** 'pwn.college{EI1W1ooLzTtBS27yj_sHqZNVYq8.QX1cjM1wCO1gjNzEzW}'      

Here,we are asked to run '/challenge/run' which will run the win command by its bare name,but it needs to have the '/challenge/more_commands/' directory as its PATH.Hence,there arises a need to manipulate the PATH variable.Hence we use 'export PATH=/challenge/more_commands' to switch the PATH to the certain directory and we use the '&&' command  to connect the first argument to the next argument which is '/challenge/run'.Now since the path is changed,win aka '/challenge/run' can run successfully giving us the flag output.     
'''      
Connected!                                                                              
hacker@path~setting-path:~$ export PATH=/challenge/more_commands/ && /challenge/run        
Invoking 'win'....        
Congratulations! You properly set the flag and 'win' has launched!        
pwn.college{EI1W1ooLzTtBS27yj_sHqZNVYq8.QX1cjM1wCO1gjNzEzW}        
hacker@path~setting-path:~$         
'''     

## What I Learnt
I learnt how to manipulate the PATH variable to a certain directory such that certain commands can be executed that require the directory to be its path with the help of 'export' command.     

## References 
None.        


<img width="750" height="126" alt="image" src="https://github.com/user-attachments/assets/84c8787e-efb3-4abf-8f63-189090c11423" />
