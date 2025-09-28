# Killing Processes
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'kill' command to get the desired output.     

## My Solve
**Flag:** 'pwn.college{wsOfAuP5PirArN_4b9rfTxFHtXh.QXyQDO0wCO1gjNzEzW}'      

Here,we are asked to run the '/challenge/run' to get the flag output,but that is not possible until '/challenge/dont_run' is killed ie.stopped.Hence we can use the 'kill' command here,which is used to kill the processes and it takes the PID as argument.Hence we use 'ps -ef' to see all the processes and find out the one we have to delete.We find the PID which in this case is 136 and we give 'kill 136' successfully killing that process.After that,when we run '/challenge/run' we get the flag output.     
'''      
Connected!                                                                            
hacker@processes~killing-processes:~$ ps -ef     
UID          PID    PPID  C STIME TTY          TIME CMD      
root           1       0  0 11:58 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h     
root           7       1  0 11:58 ?        00:00:00 /run/dojo/bin/sleep 6h     
root         135       1  0 11:58 ?        00:00:00 su -c /challenge/.launcher hacker     
hacker       136     135  0 11:58 ?        00:00:00 /challenge/dont_run     
hacker       137     136  0 11:58 ?        00:00:00 sleep 6h     
hacker       139       0  0 11:58 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint     
hacker       145       0  0 11:58 pts/1    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint     
hacker       151     139  0 11:58 pts/0    00:00:00 /run/dojo/bin/bash --login      
hacker       152     145  0 11:58 pts/1    00:00:00 /run/dojo/bin/bash --login      
hacker       178       1  0 11:58 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.0 --writable -t disableLeaveAlert true /run/dojo/bin/bash        
hacker       182     178  0 11:58 pts/2    00:00:00 /run/dojo/bin/bash --login      
hacker       192     152  0 11:58 pts/1    00:00:00 ps -ef     
hacker@processes~killing-processes:~$ kill 136     
hacker@processes~killing-processes:~$ /challenge/run     
Great job! Here is your payment:     
pwn.college{wsOfAuP5PirArN_4b9rfTxFHtXh.QXyQDO0wCO1gjNzEzW}     
hacker@processes~killing-processes:~$       
'''     

## What I Learnt
I learnt the use of 'kill' command which can be used to kill(stop) the processes from continuing in the terminal done with the help of PID as argument.     

## References 
None.     


<img width="1440" height="290" alt="image" src="https://github.com/user-attachments/assets/9214a74e-74c2-4986-be23-15d4710f2d03" />


