# Understanding Shebangs
The challenge asks you to open the terminal in the pwn.college DOJO and invoke shebangs to obtain desired results.      

## My Solve
**Flag:** 'pwn.college{oPzs1j8sBllBchhftE2j7isi-mb.0VOzMDOxwCO1gjNzEzW}'      

Here,we use shebangs to define a file's interpretation.Sometimes linux will be forced to run scripts that aren’t bash's but from python or some other language.During such situations we use shebangs,a phrase of different symbols/characters that lets linux know what kind of file it is interpreting,in this case #!/bin/bash for bash scripts.Hence,we are asked to create a shebang for bash script and print the term "hack the planet" which is done using the 'echo' command in a file editor.Once done,we check for its permissions using 'ls -l' command.We see that no users have execute permissions.Since hacker is the user we can use 'chmod u+x' give execute permissions to the user.After that,we run '/challenge/run' which checks for all conditions and once satisfied,provides the flag value.    
'''      
Connected!                                                                            
hacker@chaining~understanding-shebangs:~$ ls -l solve.sh    
-rw-r--r-- 1 hacker hacker 35 Sep 30 04:48 solve.sh    
hacker@chaining~understanding-shebangs:~$ chmod u+x solve.sh    
hacker@chaining~understanding-shebangs:~$ /challenge/run    
Testing your script...    
Perfect! Your flag:    
Flag: pwn.college{oPzs1j8sBllBchhftE2j7isi-mb.0VOzMDOxwCO1gjNzEzW}    
    
hacker@chaining~understanding-shebangs:~$     
'''    

## What I Learnt
I learnt the use of shebangs which are phrase of symbols/characters that define what kind of file linux has to run so that it can be interpreted correctly.    

## References
None.      


<img width="551" height="157" alt="image" src="https://github.com/user-attachments/assets/a81fcdeb-18d8-4fca-92aa-0ac9ef1c12ce" />      



<img width="1073" height="581" alt="image" src="https://github.com/user-attachments/assets/f04079b2-0e79-420e-bf35-89aa2a08314b" />
