# Matching with []
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '[]' globbing to get desired output......      

## My Solve
**Flag:** 'pwn.college{wwH9HmEsMC8ij9eiVE--t_yCnag.QXzIDO0wCO1gjNzEzW}'        

Here we use the '[]' globbing in terminal.Here,'[]' is a subset of potential wildcards where it checks all the files for the wildcard characters.Here we are instructed to switch to the '/challenge/files' directory.Then we are asked to run the '/challenge/run' along with an argument that checks for files file_b,file_a,file_s,file_h.So we run the command '/challenge/run file_[bash]' to get the desired output.     
'''     
Connected!                                                                              
hacker@globbing~matching-with-:~$ cd /challenge/files      
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]       
You got it! Here is your flag!      
pwn.college{wwH9HmEsMC8ij9eiVE--t_yCnag.QXzIDO0wCO1gjNzEzW}        
hacker@globbing~matching-with-:/challenge/files$          
'''    

## What I Learnt
I learnt the use of '[]' globbing which can store a set of wildcards for checking files for multiple conditions.      

## References
None.   


<img width="566" height="95" alt="image" src="https://github.com/user-attachments/assets/f3dba973-4a29-4398-a077-d0a624b8b1cb" />


