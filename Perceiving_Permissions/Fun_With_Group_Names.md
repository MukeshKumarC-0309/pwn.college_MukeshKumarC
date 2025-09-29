# Fun with group names
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'id' and 'chgrp' commands to get the desired output.     

## My Solve
**Flag:** 'pwn.college{wWXX-4LFjNjX9j3Ma-lAaazRkAH.QXycjM1wCO1gjNzEzW}'       

Here,we are asked to switch to the group which as permissions to run '/flag',but it’s hidden/renamed.Hence we use the 'id' command to find the right group name,in this case being 'grp15240'.Hence we use the 'chgrp' command to shift to that group to gain access to the '/flag' file.After using 'chgrp grp15240 /flag' command,if we run 'cat /flag' we can get the final flag output.      
'''       
Connected!                                                                            
hacker@permissions~fun-with-groups-names:~$ id        
uid=1000(hacker) gid=1000(grp15240) groups=1000(grp15240)        
hacker@permissions~fun-with-groups-names:~$ chgrp grp15240 /flag      
hacker@permissions~fun-with-groups-names:~$ cat /flag         
pwn.college{wWXX-4LFjNjX9j3Ma-lAaazRkAH.QXycjM1wCO1gjNzEzW}        
hacker@permissions~fun-with-groups-names:~$          
'''      

## What I learnt
I learnt the use of 'id' command which specifies the user name and the group in which the user is present along with the group and user ID.      

## References
None.       



<img width="747" height="108" alt="image" src="https://github.com/user-attachments/assets/53337573-b7d9-4740-88bf-ccad39ea00aa" />
