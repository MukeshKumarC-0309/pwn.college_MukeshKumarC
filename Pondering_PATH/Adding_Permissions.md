# Adding Permissions
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'chmod' and 'nano' comamnd to obtain the desired result.    

## My Solve
**Flag:** 'pwn.college{g_p0AQQIDrDxQTpi85ia4YBresG.QX2cjM1wCO1gjNzEzW}'

Here,we are asked to create a command 'win' so that the file '/challenge/run' and simultaneously make sure that the 'cat' command is not deleted while changing paths.Hence,we take the path of the 'cat' command and place our win command in the same directory.We use the 'which' command to figure out the path of the 'cat' command.Using nano,an editor we create a file named win and place the path there and add '/flag' so that it can read the flag.Then we enable execute permissions for users using the 'chmod' command.Next,we change the PATH to /home/hacker so that win command can be executed.Finally,when we use '/challenge/run' we get the flag output.     
'''      
Connected!                                                                        
hacker@path~adding-commands:~$ which cat
/run/dojo/bin/cat
hacker@path~adding-commands:~$ nano win
hacker@path~adding-commands:~$ chmod a+x win
hacker@path~adding-commands:~$ PATH=/home/hacker
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{g_p0AQQIDrDxQTpi85ia4YBresG.QX2cjM1wCO1gjNzEzW}
hacker@path~adding-commands:~$ 
'''    

## What I Learnt
I learnt the use of nano,a text editor and the methods to create a command of our own and enabling permissions for that user.    

## References
None.       

<img width="750" height="150" alt="image" src="https://github.com/user-attachments/assets/cd0b4cca-4564-4c5b-92d0-a4482d92fab3" />
