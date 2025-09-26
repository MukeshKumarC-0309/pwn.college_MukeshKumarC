# Searching for manuals
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'man' command to get the desired output.    

## My Solve
**Flag:** 'pwn.college{g_lWBmUENG8kKFTlwtLvKh36hss.QX2EDO0wCO1gjNzEzW}'    

Here,we use the 'man' command with 'man' as the arguement itself because the original manpage is hidden.On reading the manual we come across the '-k' arguement which gives the details of the command passed as arguement.Hence on passing 'man -k /challenge/challenge' we get a output which states 'glmklwtvhh (1)       - print the flag!'.Here glmktwtvhh is the arguement with 1 as the section number.Hence we put 'man 1 glmktwtvhh' command which shows us the argument which has to be passed to print the flag which is '--glmklw NUM' where NUM should be 836.Finally,we run the '/challenge/challenge  --glmklw 836' command which gives us the final flag output.   
'''    
hacker@man~searching-for-manuals:~$ man man       
hacker@man~searching-for-manuals:~$ man -k /challenge/challenge     
glmklwtvhh (1)       - print the flag!      
hacker@man~searching-for-manuals:~$ man 1 glmklwtvhh     
hacker@man~searching-for-manuals:~$ /challenge/challenge  --glmklw 836          
Correct usage! Your flag: pwn.college{g_lWBmUENG8kKFTlwtLvKh36hss.QX2EDO0wCO1gjNzEzW}       
hacker@man~searching-for-manuals:~$         
'''    

## What I Learnt
I learnt the usage of 'man' command across various arguements to check for the manual of various commands/files.   

## References
None.     

<img width="620" height="105" alt="image" src="https://github.com/user-attachments/assets/3121f4f7-9551-4a6a-8fd1-143c5a105b4d" />
