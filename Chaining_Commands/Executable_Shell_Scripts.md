# Executable Shell Scripts
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the implicit use of 'bash' command to get the desired output.     

## My Solve
**Flag:** 'pwn.college{EzDPNm6Sg8XLr090shnd-6SNQXF.QX0cjM1wCO1gjNzEzW}'     

Here,we are asked to run a script shell without calling the 'bash' command.This is possible if it’s an executable file and all we have to do is to mention the absolute/relative file path to execute a shell script.Here,we are asked to run '/challenge/solve' through a script shell and then run it without invoking the 'bash' command.Hence after the creation of the shell script using a text editor,we use 'ls -l' command to check for permissions.Since no user has permission to execeute the file,we use 'chmod a+x' to make it executable and then succesfully run the script shell to get the flag output.     
'''      
Connected!                                                                            
hacker@chaining~executable-shell-scripts:~$ ls -l test.sh      
-rw-r--r-- 1 hacker hacker 17 Sep 30 04:38 test.sh        
hacker@chaining~executable-shell-scripts:~$ chmod a+x test.sh    
hacker@chaining~executable-shell-scripts:~$ /home/hacker/test.sh    
Congratulations on your shell script execution! Your flag:    
pwn.college{EzDPNm6Sg8XLr090shnd-6SNQXF.QX0cjM1wCO1gjNzEzW}    
hacker@chaining~executable-shell-scripts:~$     
'''    

## What I Learnt
I learnt that we can execute shells scripts directly from the terminal without using the 'bash' command if the file is an executable file.   

## References
None.      

<img width="607" height="126" alt="image" src="https://github.com/user-attachments/assets/39e09860-bf65-47fc-a989-deea3c85d129" />    


<img width="1073" height="581" alt="image" src="https://github.com/user-attachments/assets/928ad1c4-50ea-40d6-95b9-55b9ae63acdf" />

