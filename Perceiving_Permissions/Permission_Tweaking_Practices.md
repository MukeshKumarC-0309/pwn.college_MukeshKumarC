# Permission Tweaking Practices
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'chmod' command to get the desired results.    

## My Solve
**Flag:** 'pwn.college{EUugJG8xLYvb_fORPHo6QzKzeXq.QXwEjN0wCO1gjNzEzW}'     

Here,we use the 'chmod' command in the terminal.The 'chmod' command is used to modify file permissions.Here,we are tasked with 8 different challenges with adding/removing different permissions for different types of user such as removing execute commands for users etc.Finishing all 8 challenges unlocks the '/flag' file as it specifies the permissions for it which is none.Hence to read the file,we use the command 'chmod a+r /challenge/pwn' to enable read permissions for all users,and we run the command 'cat /flag' to get the final flag output.      
'''              
Connected!                                                                              
hacker@permissions~permission-tweaking-practice:~$ /challenge/run              
Round 1 of 8!           
     
Current permissions of "/challenge/pwn": rw-r--r--    
* the user does have read permissions    
* the user does have write permissions    
- the user doesn't have execute permissions    
* the group does have read permissions    
- the group doesn't have write permissions    
- the group doesn't have execute permissions    
* the world does have read permissions    
- the world doesn't have write permissions    
- the world doesn't have execute permissions    
    
Needed permissions of "/challenge/pwn": rw-rw-r--   
* the user does have read permissions    
* the user does have write permissions     
- the user doesn't have execute permissions   
* the group does have read permissions     
* the group does have write permissions   
- the group doesn't have execute permissions   
* the world does have read permissions   
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
hacker@permissions~permission-tweaking-practice:~$ chmod g+w /challenge/pwn   
You set the correct permissions!    
Round 2 of 8!    
    
Current permissions of "/challenge/pwn": rw-rw-r--   
* the user does have read permissions   
* the user does have write permissions   
- the user doesn't have execute permissions     
* the group does have read permissions   
* the group does have write permissions    
- the group doesn't have execute permissions    
* the world does have read permissions    
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
  
Needed permissions of "/challenge/pwn": r--rw-r--   
* the user does have read permissions   
- the user doesn't have write permissions   
- the user doesn't have execute permissions    
* the group does have read permissions     
* the group does have write permissions   
- the group doesn't have execute permissions   
* the world does have read permissions   
- the world doesn't have write permissions    
- the world doesn't have execute permissions    
hacker@permissions~permission-tweaking-practice:~$ chmod u-w /challenge/pwn   
You set the correct permissions!    
Round 3 of 8!    
   
Current permissions of "/challenge/pwn": r--rw-r--   
* the user does have read permissions   
- the user doesn't have write permissions   
- the user doesn't have execute permissions   
* the group does have read permissions   
* the group does have write permissions   
- the group doesn't have execute permissions   
* the world does have read permissions   
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
   
Needed permissions of "/challenge/pwn": ----w----    
- the user doesn't have read permissions    
- the user doesn't have write permissions    
- the user doesn't have execute permissions    
- the group doesn't have read permissions    
* the group does have write permissions    
- the group doesn't have execute permissions     
- the world doesn't have read permissions   
- the world doesn't have write permissions    
- the world doesn't have execute permissions    
hacker@permissions~permission-tweaking-practice:~$ chmod a-r /challenge/pwn     
You set the correct permissions!     
Round 4 of 8!     
    
Current permissions of "/challenge/pwn": ----w----   
- the user doesn't have read permissions    
- the user doesn't have write permissions    
- the user doesn't have execute permissions   
- the group doesn't have read permissions   
* the group does have write permissions    
- the group doesn't have execute permissions   
- the world doesn't have read permissions   
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
    
Needed permissions of "/challenge/pwn": ---------    
- the user doesn't have read permissions   
- the user doesn't have write permissions   
- the user doesn't have execute permissions   
- the group doesn't have read permissions   
- the group doesn't have write permissions   
- the group doesn't have execute permissions   
- the world doesn't have read permissions   
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
hacker@permissions~permission-tweaking-practice:~$ chmod g-w /challenge/pwn   
You set the correct permissions!    
Round 5 of 8!   
   
Current permissions of "/challenge/pwn": ---------    
- the user doesn't have read permissions    
- the user doesn't have write permissions   
- the user doesn't have execute permissions  
- the group doesn't have read permissions   
- the group doesn't have write permissions   
- the group doesn't have execute permissions   
- the world doesn't have read permissions   
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
    
Needed permissions of "/challenge/pwn": ---r--r--    
- the user doesn't have read permissions   
- the user doesn't have write permissions   
- the user doesn't have execute permissions    
* the group does have read permissions  
- the group doesn't have write permissions   
- the group doesn't have execute permissions   
* the world does have read permissions   
- the world doesn't have write permissions   
- the world doesn't have execute permissions   
hacker@permissions~permission-tweaking-practice:~$ chmod go+r /challenge/pwn   
You set the correct permissions!   
Round 6 of 8!   
   
Current permissions of "/challenge/pwn": ---r--r--   
- the user doesn't have read permissions   
- the user doesn't have write permissions   
- the user doesn't have execute permissions   
* the group does have read permissions  
- the group doesn't have write permissions  
- the group doesn't have execute permissions   
* the world does have read permissions  
- the world doesn't have write permissions  
- the world doesn't have execute permissions   
    
Needed permissions of "/challenge/pwn": -wxr--rwx  
- the user doesn't have read permissions  
* the user does have write permissions  
* the user does have execute permissions  
* the group does have read permissions  
- the group doesn't have write permissions  
- the group doesn't have execute permissions  
* the world does have read permissions  
* the world does have write permissions  
* the world does have execute permissions  
hacker@permissions~permission-tweaking-practice:~$ chmod uo+wx /challenge/pwn  
You set the correct permissions!    
Round 7 of 8!  
  
Current permissions of "/challenge/pwn": -wxr--rwx  
- the user doesn't have read permissions  
* the user does have write permissions  
* the user does have execute permissions  
* the group does have read permissions  
- the group doesn't have write permissions  
- the group doesn't have execute permissions  
* the world does have read permissions  
* the world does have write permissions  
* the world does have execute permissions  
  
Needed permissions of "/challenge/pwn": -w-r--rwx  
- the user doesn't have read permissions  
* the user does have write permissions  
- the user doesn't have execute permissions  
* the group does have read permissions  
- the group doesn't have write permissions  
- the group doesn't have execute permissions  
* the world does have read permissions  
* the world does have write permissions  
* the world does have execute permissions  
hacker@permissions~permission-tweaking-practice:~$ chmod u-x /challenge/pwn  
You set the correct permissions!  
Round 8 of 8!  
  
Current permissions of "/challenge/pwn": -w-r--rwx   
- the user doesn't have read permissions   
* the user does have write permissions   
- the user doesn't have execute permissions  
* the group does have read permissions   
- the group doesn't have write permissions   
- the group doesn't have execute permissions   
* the world does have read permissions   
* the world does have write permissions   
* the world does have execute permissions    
      
Needed permissions of "/challenge/pwn": -w-r-xrwx     
- the user doesn't have read permissions         
* the user does have write permissions     
- the user doesn't have execute permissions     
* the group does have read permissions      
- the group doesn't have write permissions     
* the group does have execute permissions     
* the world does have read permissions     
* the world does have write permissions     
* the world does have execute permissions           
hacker@permissions~permission-tweaking-practice:~$ chmod g+x /challenge/pwn        
You set the correct permissions!      
You've solved all 8 rounds! I have changed the ownership     
of the /flag file so that you can 'chmod' it. You won't be able to read     
it until you make it readable with chmod!      
     
Current permissions of "/flag": ---------       
- the user doesn't have read permissions      
- the user doesn't have write permissions      
- the user doesn't have execute permissions      
- the group doesn't have read permissions     
- the group doesn't have write permissions      
- the group doesn't have execute permissions      
- the world doesn't have read permissions     
- the world doesn't have write permissions      
- the world doesn't have execute permissions     
hacker@permissions~permission-tweaking-practice:~$ chmod a+r /flag      
hacker@permissions~permission-tweaking-practice:~$ cat /flag       
pwn.college{EUugJG8xLYvb_fORPHo6QzKzeXq.QXwEjN0wCO1gjNzEzW}      
hacker@permissions~permission-tweaking-practice:~$
'''

## What I Learnt
I learnt the further usage of 'chmod' command which can be used 'n' number of times to change the file permissions for different types of users.     

## References
None.       

<img width="611" height="900" alt="image" src="https://github.com/user-attachments/assets/1c004f71-48bb-4acd-ad6b-83625d68cf99" />     


<img width="611" height="900" alt="image" src="https://github.com/user-attachments/assets/90f14108-1e68-4fa9-bb78-c50050ed80c3" />      


<img width="611" height="900" alt="image" src="https://github.com/user-attachments/assets/d3790a13-c3c5-4f41-b839-cd97d556ff42" />      


<img width="611" height="869" alt="image" src="https://github.com/user-attachments/assets/96bf31d0-cebc-4d51-ab26-d60c2de527e5" />



