# Building On Success
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '&&' command to get the desired output.       

## My Solve
**Flag:** 'pwn.college{IkoumALnwAD3p15lh7-70yvci28.0lM0MDOxwCO1gjNzEzW}'     

Here,we use the '&&' command in the terminal.The '&&' is used to run 2 or more processes only if the previous run successfully(checked using exit codes).Here we are asked to '/challenge/first-success' and '/challenge/second' only if the first one is run successfully.Running them individually did not work and gave us error stating the use of '&&'.Hence,we use '/challenge/first-success && /challenge/second' and both of them run successfully giving us the flag.     
'''    
Connected!        
hacker@chaining~building-on-success:~$ /challenge/first-success         
hacker@chaining~building-on-success:~$ /challenge/second       
Error: /challenge/first-success must be successfully chained with        
/challenge/second using &&         
hacker@chaining~building-on-success:~$ /challenge/first-success && /challenge/second          
Nice chaining! Flag: pwn.college{IkoumALnwAD3p15lh7-70yvci28.0lM0MDOxwCO1gjNzEzW}        
hacker@chaining~building-on-success:~$           
'''     

## What I Learnt
I learnt the use of '&&' command which is used as an 'and' operator which can be used to check if one program is running successfully and if yes,the second command is run.        

## References
None.         

<img width="636" height="122" alt="image" src="https://github.com/user-attachments/assets/3f0dbf68-5c2f-41bb-8c10-15c5dd07d5f0" />
