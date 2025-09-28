# Listing Processes
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'ps' command to get the desired result.      

## My Solve
**Flag:** 'pwn.college{gNcXtUJgJb4eLH3wHntiaBeaw7I.QX4MDO0wCO1gjNzEzW}'      

Here,we are asked to run the '/challenge/run' file to get the flag output,but this time it has been renamed and hidden elsewhere.Fortunately,it is given that it is already running which means there's a log of it in the terminal.Here,we can use the 'ps' command.The 'ps' command lists all the process that are happening in the terminal.Giving 'ps -ef' gives some extra information about the processes.Hence when the list of processes is shown,we find a file that's close to the challenge file named '/challenge/14037-run-27870',which when run gives us the flag output.    
'''     
Connected!                                                                           
hacker@processes~listing-processes:~$ ps -ef       
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  1 11:45 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h       
root           8       1  0 11:45 ?        00:00:00 /run/dojo/bin/sleep 6h       
root         133       1  0 11:45 ?        00:00:00 /challenge/14037-run-27870      
root         136     133  0 11:45 ?        00:00:00 sleep 6h       
hacker       138       0  1 11:45 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint       
hacker       144     138  0 11:45 pts/0    00:00:00 /run/dojo/bin/bash --login       
hacker       162       1  0 11:45 ?        00:00:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.7/bin/ttyd --port 7681 --interface 0.0.0.0 --writable -t disableLeaveAlert true /run/dojo/bin/bash        
hacker       166     144  0 11:45 pts/0    00:00:00 ps -ef     
hacker@processes~listing-processes:~$ /challenge/14037-run-27870    
Yahaha, you found me! Here is your flag:    
pwn.college{gNcXtUJgJb4eLH3wHntiaBeaw7I.QX4MDO0wCO1gjNzEzW}     
Now I will sleep for a while (so that you could find me with 'ps').     
'''     

## What I Learnt
I learnt the usage of 'ps' command and its prompts which are used to give the list of processes happening in the terminal along with extra details about the processes.     

## References
None.    


<img width="1440" height="237" alt="image" src="https://github.com/user-attachments/assets/27e5abde-2b43-4700-899a-8fd09b430ec3" />
