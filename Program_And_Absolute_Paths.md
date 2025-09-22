# Program and absolute paths
The challenge asks you to open the terminal in the pwn.college DOJO and use the ' / ' command to specify an absolute path to get desired result

## My Solve
**Flag:** 'pwn.college{oOA0XD0dNd-WXIZXJPDxVYAe2wR.QX1QTN0wCO1gjNzEzW}'  

Here,we have been told that the flag is hidden in the challenge directory and we need to access that specific file.Hence we use the ' / ' command to specify the absolute path which was '/challenge/run' and which on doing so gaves us the required flag.   
'''   
hacker@paths~program-and-absolute-paths:~$ /challenge/run    
Correct!!!     
/challenge/run is an absolute path! Here is your flag:      
pwn.college{oOA0XD0dNd-WXIZXJPDxVYAe2wR.QX1QTN0wCO1gjNzEzW}     
hacker@paths~program-and-absolute-paths:~$     
'''   

## What I learnt
I learnt that files can be stored in directories which in turn can be stored in other directories and so on....and to the access the file all we have to do is to use the '/' command to specify the absolute file path in which it is stored.   

## References
None.  

<img width="753" height="81" alt="Screenshot 2025-09-22 at 7 48 06 PM" src="https://github.com/user-attachments/assets/0f8ce25b-5888-4276-b978-a309ffae0258" />


