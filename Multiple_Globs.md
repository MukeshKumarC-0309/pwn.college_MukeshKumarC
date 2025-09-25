# Multiple Globs
The challenge asks you to open the terminal in the pwn.college DOJO and invoke multiple globbing to obtain desired results.        

## My Solve
**Flag:** 'pwn.college{oW5D5fwdEkCJD9BZDc3OwcRrERS.0lM3kjNxwCO1gjNzEzW}'      

Here we are asked to run the 'challenge/run' command as usual but with an argument with multiple globbings,not more than 3 characters,and opens the files which has the letter 'p' in them.Multiple globbings can be achieved by using '*' in multiple instances.Hence we run the '/challenge/run *p*' command where *p* indicates any file that starts with anything,has the letter 'p' in it and ends with anything,which gives us the flag output.    
'''     
Connected!                                                                            
hacker@globbing~multiple-globs:~$ cd /challenge/files    
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*     
You got it! Here is your flag!      
pwn.college{oW5D5fwdEkCJD9BZDc3OwcRrERS.0lM3kjNxwCO1gjNzEzW}       
hacker@globbing~multiple-globs:/challenge/files$          
'''    

## What I Learnt
I learnt the usage of multiple globbings,using '*' in multiple instances which let us specify file paths with more complex conditions.   

## References
None.    

<img width="608" height="95" alt="image" src="https://github.com/user-attachments/assets/22340cc3-02eb-448d-919e-1041ea4959e6" />
