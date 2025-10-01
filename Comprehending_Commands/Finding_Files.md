# Finding Files
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'find' command to obtain the desired result.       

## My Solve
**Flag:** 'pwn.college{QKSuDD7Z6Xw3EQwr7iN1qzCEG9L.QXyMDO0wCO1gjNzEzW}'      

Here,we use the 'find' command in the terminal.The 'find' command is used to search for files in the directories.It can search a specific directory or the entire filesystem depending on what argument we give.Here,we have to find the file named flag,hence we use the command 'find / -name flag' so that it searches the entire filesystem for a file named 'flag'.Once done,it shows a list of all the files which have the name 'flag' in them.One among them is '/usr/lib/R/etc/flag' which could be our flag.Hence we read it using the 'cat' command.It works,displaying the flag.     
'''        
Connected!                                                                            
hacker@module-1~finding-files:~$ find / -name flag        
find: ‘/tmp/tmp.4mK6TfTSUV’: Permission denied        
find: ‘/etc/ssl/private’: Permission denied      
/usr/lib/R/etc/flag        
/usr/local/lib/python3.8/dist-packages/pwnlib/flag        
find: ‘/var/cache/apt/archives/partial’: Permission denied        
find: ‘/var/cache/ldconfig’: Permission denied        
find: ‘/var/cache/private’: Permission denied      
find: ‘/var/lib/apt/lists/partial’: Permission denied        
find: ‘/var/lib/mysql-files’: Permission denied        
find: ‘/var/lib/private’: Permission denied        
find: ‘/var/lib/mysql’: Permission denied          
find: ‘/var/lib/mysql-keyring’: Permission denied        
find: ‘/var/lib/php/sessions’: Permission denied        
find: ‘/var/log/private’: Permission denied        
find: ‘/var/log/apache2’: Permission denied        
find: ‘/var/log/mysql’: Permission denied        
find: ‘/run/mysqld’: Permission denied          
find: ‘/run/sudo’: Permission denied          
find: ‘/root’: Permission denied        
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag        
find: ‘/proc/tty/driver’: Permission denied        
find: ‘/proc/1/task/1/fd’: Permission denied        
find: ‘/proc/1/task/1/fdinfo’: Permission denied        
find: ‘/proc/1/task/1/ns’: Permission denied        
find: ‘/proc/1/fd’: Permission denied        
find: ‘/proc/1/map_files’: Permission denied          
find: ‘/proc/1/fdinfo’: Permission denied        
find: ‘/proc/1/ns’: Permission denied        
find: ‘/proc/7/task/7/fd’: Permission denied        
find: ‘/proc/7/task/7/fdinfo’: Permission denied      
find: ‘/proc/7/task/7/ns’: Permission denied        
find: ‘/proc/7/fd’: Permission denied        
find: ‘/proc/7/map_files’: Permission denied        
find: ‘/proc/7/fdinfo’: Permission denied        
find: ‘/proc/7/ns’: Permission denied          
/nix/store/ka6xbd6z6wj5d6frl7ym4nzfc6p2wkdx-radare2-5.9.8/share/radare2/5.9.8/flag        
/nix/store/f31j0igg7ms3yrj5gm3cm76bjcmdl8w5-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag        
/nix/store/7ns27apnvn4qj4q5c82x0z1lzixrz47p-radare2-5.9.8/share/radare2/5.9.8/flag          
/nix/store/5z3sjp9r463i3siif58hq5wj5jmy5m98-python3.12-pwntools-4.13.1/lib/python3.12/site-packages/pwnlib/flag        
/nix/store/n6vb30rd7kkwjj595pgm0dmsmfaqi6i5-rizin-0.7.3/share/rizin/flag        
/nix/store/5n5lp1m8gilgrsriv1f2z0jdjk50ypcn-rizin-0.7.3/share/rizin/flag        
/nix/store/bnlabj2vsbljhp597ir29l51nrqhm89w-rizin-0.7.4/share/rizin/flag        
/nix/store/s8b49lb0pqwvw0c6kgjbxdwxcv2bp0x4-radare2-5.9.8/share/radare2/5.9.8/flag        
/nix/store/8qvj9mzdq2qxgjigw4ysqgbkcx1zi80y-python3.13-pwntools-4.14.1/lib/python3.13/site-packages/pwnlib/flag          
/nix/store/1hyxipvwpdpcxw90l5pq1nvd6s6jdi5m-python3.12-pwntools-4.14.1/lib/python3.12/site-packages/pwnlib/flag            
/nix/store/dz2qxywk6d8hc1gkarpwbhyxb50sh2ak-pwntools-4.14.0/lib/python3.13/site-packages/pwnlib/flag                
hacker@module-1~finding-files:~$ cat /usr/lib/R/etc/flag            
pwn.college{QKSuDD7Z6Xw3EQwr7iN1qzCEG9L.QXyMDO0wCO1gjNzEzW}hacker@module-1~finding-files:~$           
'''      

## What I Learnt 
I learnt the use of 'find' command which can be used to find a file in a specific directory or the entire filesystem depending on the arguments given.      

## References
None.              


<img width="944" height="711" alt="image" src="https://github.com/user-attachments/assets/458f2527-d263-449a-b02a-65a2b8d8cb96" />
