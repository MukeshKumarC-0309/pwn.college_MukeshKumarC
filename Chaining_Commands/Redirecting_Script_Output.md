# Redirecting Script Output
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'bash' command and piping to get the desired output.    

## My Solve
**Flag:** 'pwn.college{cIDHk4ZL1I0tSNaYSxvSH6r-vCK.QX4ETO0wCO1gjNzEzW}'      

Here,we are asked to redirect the output to another file.This can be done using piping wherein the output of the first command is the input of the 2nd command.Hence we create a file in the text editor and place '/challenge/pwn && /challenge/college' so that they are execeuted simultaneously and save it with a '.sh' extension.Next,we use the 'bash' command to access the script and use '|' to pipe the output to '/challenge/solve'.Hence our final input ie.'bash chal.sh | /challenge/solve' is executed successfully giving us the flag value.   
'''     
Connected!                                                                            
hacker@chaining~redirecting-script-output:~$ bash chal.sh | /challenge/solve    
Correct! Here is your flag:    
pwn.college{cIDHk4ZL1I0tSNaYSxvSH6r-vCK.QX4ETO0wCO1gjNzEzW}      
hacker@chaining~redirecting-script-output:~$       
'''    

## What I Learnt
I learnt that in addition to redirecting command outputs,we can use piping to redirect script outputs alo with the corresponding arguments.      

## References
None.     

<img width="590" height="85" alt="image" src="https://github.com/user-attachments/assets/f60a4c99-7128-4640-908d-b3ce7ce39f1d" />    


<img width="1071" height="585" alt="image" src="https://github.com/user-attachments/assets/d384ca10-daa1-4b52-810a-fce8bd0d89f3" />

