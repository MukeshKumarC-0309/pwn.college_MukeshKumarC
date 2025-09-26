# Matching Paths with []
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '[]' globbing with a file path to obtain desired output.     

## My Solve
**Flag:** 'pwn.college{Evu9BqiG248s5qurTL9OSj_os7i.QX0IDO0wCO1gjNzEzW}'     

Here,we are instructed to run the '/challenge/run' command directly along with an argument that globs all the 4 files(file_b,file_a,file_s,file_h) from /challenge/files.Hence we run '/challenge/run /challenge/files/file_[bash]',hence getting final desired output.    
'''     
Connected!                                                                           
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]     
You got it! Here is your flag!       
pwn.college{Evu9BqiG248s5qurTL9OSj_os7i.QX0IDO0wCO1gjNzEzW}      
hacker@globbing~matching-paths-with-:~$      
'''   

## What I Learnt
I learnt the complex usage of the '[]' globbing which also takes a file path as argument in order to search for multiple files together.     

## References
None.    


<img width="608" height="95" alt="image" src="https://github.com/user-attachments/assets/c8f86cc9-f4cd-43cd-9753-32c58bda94d8" />
