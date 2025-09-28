# Exporting Variables
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'export' command to get the desired output.   

## My Solve
**Flag:** 'pwn.college{o1Hhz5XvZhNcBuI_WvxtZo676aV.QXyYTN0wCO1gjNzEzW}'    

Here,they ask us to export a variable with a set value and set another variable with a value but without exporting it.This can be done using the 'export' command.All the variables that we declare in the shell is local and will not be saved permanently,hence we can use the 'export' command to set them.So according to this challenge we need to export 'PWN' and set it to 'COLLEGE' which is done by 'export PWN=COLLEGE' and set another variable 'COLLEGE' and set it to 'PWN' which is done by 'PWN=COLLEGE'.Hence on completing both steps we can invoke the '/challenge/run' command whch succesfully gives us the flag output.    
'''     
Connected!                                                                           
hacker@variables~exporting-variables:~$ export PWN=COLLEGE     
You've set the PWN variable to the proper value!     
hacker@variables~exporting-variables:~$ COLLEGE=PWN     
You've set the PWN variable to the proper value!     
You've set the COLLEGE variable to the proper value!     
hacker@variables~exporting-variables:~$ /challenge/run     
CORRECT!     
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great     
job! Here is your flag:     
pwn.college{o1Hhz5XvZhNcBuI_WvxtZo676aV.QXyYTN0wCO1gjNzEzW}     
You've set the PWN variable to the proper value!    
You've set the COLLEGE variable to the proper value!     
hacker@variables~exporting-variables:~$      
'''   

## What I Learnt
I learnt the usage of 'export' command and local saving.'export' command is used to export variables into the environment variables.    

## References 
None.   

<img width="537" height="206" alt="image" src="https://github.com/user-attachments/assets/81abd4c4-f851-4f3c-854c-b69a85fd5f9f" />


