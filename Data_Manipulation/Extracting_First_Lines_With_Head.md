# Extracting First Lines with Head
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'head' command to get desired output.   

## My Solve
**Flag:** 'pwn.college{IkOtHoR2vUEOiVN18X3odpLeOnO.0lNxEzNxwCO1gjNzEzW}'   

Here,we are asked to open the /challenge/pwn file and check for the flag.But it has a lot of lines and it only needs the first 7 lines.This is where the 'head' command.The 'head' command is used to display only a certain number of lines presented in the argument(default value is 10).Simultaneously we also pipe the output to '/challenge/college'.Hence our final code looks like '/challenge/pwn | head -n 7 | /challenge/college' when run gives us the desired flag output.   
'''    
Connected!                                                                              
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college      
Congratulations, you piped the right codes!     
pwn.college{IkOtHoR2vUEOiVN18X3odpLeOnO.0lNxEzNxwCO1gjNzEzW}        
hacker@data~extracting-the-first-lines-with-head:~$      
'''     

## What I Learnt
I learnt the usage of 'head' command which is used to display only certain number of lines from the beginning as it makes file reading more convenient.      

## References
None.    

<img width="844" height="68" alt="image" src="https://github.com/user-attachments/assets/a563fe26-5922-4a4b-8b63-42888fd21ab3" />
