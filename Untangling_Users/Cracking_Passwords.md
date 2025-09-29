# Cracking Passwords
The challenge asks you to open the terminal in the pwn.college DOJO and invoke John the Ripper to obtain the desired result.       

## My Solve
**Flag:** 'pwn.college{sYsXJicXChg2cFS8-yesz_8Q4M_.QX3UDN1wCO1gjNzEzW}'    

Here,we are asked to switch to zardus and run the '/challenge/run' command to get the flag,but we do not know the password to zardus.Hence we take the help of John the ripper who has cracked the password to the user,by using 'john /challenge/shadow-leak'(/challenge/shadow-leak has the leak of passwords from /etc/shadow) and we wait for sometime till it cracks the password after whitch it says "session completed".After this,we run the command "john --show /challenge/shadow-leak" which is used to show all the cracked passwords,among which is the password for the user 'zardus'.Hence we use 'su zardus' and enter the password to switch to that user.Then,we run the '/challenge/run' command which succesfully gives the flag value.     
'''      
Connected!                                                                              
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak      
Loaded 1 password hash (crypt, generic crypt(3) [?/64])        
Press 'q' or Ctrl-C to abort, almost any other key for status     
aardvark         (zardus)       
1g 0:00:00:21 100% 2/3 0.04714g/s 274.5p/s 274.5c/s 274.5C/s Johnson..buzz      
Use the "--show" option to display all of the cracked passwords reliably      
Session completed       
hacker@users~cracking-passwords:~$ john --show /challenge/shadow-leak      
hacker:NO PASSWORD:20357:0:99999:7:::     
zardus:aardvark:20360:0:99999:7:::       
      
2 password hashes cracked, 0 left       
hacker@users~cracking-passwords:~$ su zardus       
Password:       
zardus@users~cracking-passwords:/home/hacker$ /challenge/run       
Congratulations, you have become Zardus! Here is your flag:        
pwn.college{sYsXJicXChg2cFS8-yesz_8Q4M_.QX3UDN1wCO1gjNzEzW}       
zardus@users~cracking-passwords:/home/hacker$          
'''       

## What I Learnt
I learnt the use of the 'john' command which can be used to crack passwords due to a leak in the '/etc/shadow' files.      

## References
None.       

<img width="747" height="284" alt="image" src="https://github.com/user-attachments/assets/5ea54417-c38f-42ca-aa22-222006d89875" />
