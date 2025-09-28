# Named Pipes
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'mkfifo' command to get the desired output.    

## My Solve
**Flag:** 'pwn.college{4XsFo02M2vqA-C6Sf1prQFOygpo.01MzMDOxwCO1gjNzEzW}'         

Here,we are asked to create a pipe of our own in the terminal.This can be done through the 'mkfifo' command,which is used to create a persistent pipe in a location we choose.Hence we create a new pipe named '/tmp/flag_fifo' using the 'mkfifo' command.Next it asks us to redirect the output of '/challenge/run' to the pipe.Hence we use the '>' command to redirect the output.But it shows that it blocks operations till it’s called from both sides ie.input and output at the same time.Hence we open a new terminal and use 'cat /tmp/flag_fifo' to achieve both sides of the pipe and it is succesfully completed giving us the flag value.     
'''    
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo      
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo     
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!     
Bash will now try to open the FIFO for writing, to pass it as the stdout of      
/challenge/run. Recall that operations on FIFOs will *block* until both the     
read side and the write side is open, so /challenge/run will not actually be     
launched until you start reading from the FIFO!     
hacker@piping~named-pipes:~$     
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo     
You've correctly redirected /challenge/run's stdout to a FIFO at      
/tmp/flag_fifo! Here is your flag:     
pwn.college{4XsFo02M2vqA-C6Sf1prQFOygpo.01MzMDOxwCO1gjNzEzW}     
hacker@piping~named-pipes:~$       
'''      

## What I Learnt
I learnt the use of 'mkfifo' command which can be used to create a persistent pipe which can be used till we delete it.    

## References
None.    


<img width="802" height="164" alt="image" src="https://github.com/user-attachments/assets/c2492f8c-1968-4df8-82e7-9f0acd84b290" />     


<img width="802" height="123" alt="image" src="https://github.com/user-attachments/assets/da3bcde0-db0a-4280-8fce-e97f3ce8249d" />

