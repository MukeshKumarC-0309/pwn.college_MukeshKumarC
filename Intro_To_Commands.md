# Intro To Commands 
The challenge asks us to open the terminal in the pwn.college DOJO and use the "hello" and "whoami" commands to obtain the flag!  

##My Solve
**flag:**'pwn.college{sA6PzR-Q1e0f63-hcnZB3nYMZx2.QX3YjM1wCO1gjNzEzW}'

First we execute the "whoami" command in the terminal.We see that the whoami command states who you are in that respective frame,in this case 'hacker' who subsequently has lesser permissions.Thereby we use the 'hello' command with no arguements to retrieve the flag  

'''
hacker@hello~intro-to-commands:~$ whoami
hacker
hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{sA6PzR-Q1e0f63-hcnZB3nYMZx2.QX3YjM1wCO1gjNzEzW}
hacker@hello~intro-to-commands:~$ 
'''

## What i learnt  
I learnt that using 'whoami' command can let us know our role in the challenge which can help us deivse a suitable plan to retieve the flag.

## References
None.

<img width="430" height="90" alt="Screenshot 2025-09-22 at 6 55 25 PM" src="https://github.com/user-attachments/assets/9e42da1d-bd9e-4dff-8a27-50ee45f65924" />
