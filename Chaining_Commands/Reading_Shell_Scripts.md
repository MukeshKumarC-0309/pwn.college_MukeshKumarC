# Reading Shell Scripts
The challenge asks you to open the terminal in the pwn.college DOJO and read the shell scripts to obtain the desired result.         

## My Solve
**Flag:** 'pwn.college{8u4-9-_RKOmBIXFqcJfVBZAYix5.0lMwgDOxwCO1gjNzEzW}'      

Here,we are asked to read shell scripts in the terminal.Just like how we write shell scripts in a text editor,we can also read the shell scripts to obtain crucial information.This is can be done using the 'cat' command because it’s written in a text editor.Hence when use the 'cat' command to read it,we see that we need to run the command '/challenge/run' and when asked for an input we must give 'hack the PLANET' for it to be succesfully executed and get the flag output.Hence we run '/challenge/run' and provide the correct input and once it’s done,it prints the flag value.    
'''      
Connected!                                                                          
hacker@chaining~reading-shell-scripts:~$ cat /challenge/run      
#!/opt/pwn.college/bash      
      
read GUESS      
if [ "$GUESS" == "hack the PLANET" ]      
then      
	echo "CORRECT! Your flag:"        
	cat /flag      
else      
	echo "Read the /challenge/run file to figure out the correct password!"        
fi        
hacker@chaining~reading-shell-scripts:~$ /challenge/run        
hack the PLANET        
CORRECT! Your flag:        
pwn.college{8u4-9-_RKOmBIXFqcJfVBZAYix5.0lMwgDOxwCO1gjNzEzW}          
hacker@chaining~reading-shell-scripts:~$         
'''     

## What I learnt 
I leanrt that we can read shell scripts using the 'cat' command as it’s a type of text file and this can be used to read through the scripts and extract any information if necessary.     

## References
None.     

<img width="922" height="251" alt="image" src="https://github.com/user-attachments/assets/e08ac61e-d251-4b2b-90e2-9a9982ccd76d" />    
