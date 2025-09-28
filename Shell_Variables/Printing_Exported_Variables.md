# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'env' command to get the desired result.    

## My Solve
**Flag:** 'pwn.college{0gvR5g7dJHusDmDQUyctEXRu1B_.QX4UTN0wCO1gjNzEzW}'    

Here,we are asked to access all the variables in the bash,more specifically all the exported variables.We learn another method to see them ie.'env' command which prints all the exported variables.Hence on running 'env' command it shows us the list of all exported variables,among which is the 'FLAG' variable which contains the flag output.    
'''   
Connected!                                                                           
hacker@variables~printing-exported-variables:~$ env    
SHELL=/run/dojo/bin/bash     
HOSTNAME=variables~printing-exported-variables     
PWD=/home/hacker    
MANPATH=/run/dojo/share/man:     
DOJO_AUTH_TOKEN=68826ffcef3704915eba0cfe956c69b5254048df05c3e57f44c36288aa5ef540     
HOME=/home/hacker     
LANG=C.UTF-8     
FLAG=pwn.college{0gvR5g7dJHusDmDQUyctEXRu1B_.QX4UTN0wCO1gjNzEzW}     
TERMINFO=/run/dojo/share/terminfo      
TERM=xterm-256color     
SHLVL=2     
LC_CTYPE=C.UTF-8      
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt      
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin     
DEBIAN_FRONTEND=noninteractive     
_=/run/dojo/bin/env     
hacker@variables~printing-exported-variables:~$       
'''    

## What I Learnt
I learnt the usage of 'env' command which is used to print all the exported variables in the bash shell in the terminal.    

## References
None.     


<img width="833" height="281" alt="image" src="https://github.com/user-attachments/assets/56828a56-7aaa-40fa-b710-aa22bd884ec7" />
