# Matching with ?
The challenge asks you to open the terminal in the pwn.college DOJO and invoke globbing to get the desired output.    

## My Solve
**Flag:** 'pwn.college{gHoNBpRulPPDwNDnGklPA9vt3gp.QXyIDO0wCO1gjNzEzW}'     

Here,we are instructed to use globbing to specify the file paths.Globbing is a method which is used to shorten file paths making it easier for users to acces long file paths.Here we are asked to switch to the '/challenge' directory replacing 'c' and 'l' with ?.Hence we use globbing to access the '/challenge' directory.Then we run the '/challenge/run' to get the desired output.        
'''         
Connected!                                                                             
This challenge resets your working directory to /home/hacker unless you change       
directory properly...         
This challenge resets your working directory to /home/hacker unless you change        
directory properly...     
hacker@globbing~matching-with-:~$ cd /?ha??enge      
hacker@globbing~matching-with-:/challenge$ /challenge/run      
You ran me with the working directory of /challenge! Here is your flag:        
pwn.college{gHoNBpRulPPDwNDnGklPA9vt3gp.QXyIDO0wCO1gjNzEzW}         
hacker@globbing~matching-with-:/challenge$         
'''     

## What I Learnt 
I learnt the use of globbing which is used to make the user's job easier while specifying file paths in this case using '?',which replaces a single character.      

## References
None.    


<img width="566" height="151" alt="image" src="https://github.com/user-attachments/assets/cd7a6a5b-b918-4037-81aa-a18d65225bac" />



