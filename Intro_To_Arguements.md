# Intro To Arguements  
The challenge asks us to open the terminal in the pwn.college DOJO and use the "hello" and "echo" commands with multiple arguements to obtain the flag!  

##My Solve
**flag:**'pwn.college{M5ZD6dyf3qRY0rB7uIpK1blXzHb.QX4YjM1wCO1gjNzEzW}'

First we execute the "echo" command in the terminal.We see that the echo command can take multiple arguements and act accordingly.For example,if we use 'echo hackers'(single arguement) it prints 'hackers' and instead if we give 'echo Hello Hackers!'(multiple arguements) it prints 'Hello Hackers!'.Similarly we can use the 'hello' command with a suitable arguement(ie.hackers) to obtain the flag

'''
hacker@hello~intro-to-arguments:~$ echo Hackers!
Hackers!
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{M5ZD6dyf3qRY0rB7uIpK1blXzHb.QX4YjM1wCO1gjNzEzW}
hacker@hello~intro-to-arguments:~$ 
'''
## What i learnt  
I learnt that linux commands can take up multiple arguements and how according to each arguement there's a different output corresponding to it.We also learn the use of 'echo' command which is used to print the necessary statements given as arguements.

## References
None.

<img width="430" height="90" alt="Screenshot 2025-09-22 at 7 02 05 PM" src="https://github.com/user-attachments/assets/959b733d-e52d-4914-95dd-1c40d5f45497" />
