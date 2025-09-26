# Exclusionary Globbing
The challenge asks you to open the terminal in the pwn.college DOJO and invoke globbing to obtain desired result(exlcuding files).    

## My Solve
**Flag:** 'pwn.college{4AogD_6R3i3sDwefEd2Vik_8KsR.QX2IDO0wCO1gjNzEzW}'      

We are instructed to switch to the '/challenge/files' directory and run the '/challenge/run' command along with all the files that don’t start with either p or w or n.Hence we use the concept of exclusionary globbing here.Exclusionary Globbing is the opposite of globbing wherein it shows all the files that do not satisfy the condition present in globbing,it is done with either '!' or '^' command.So since we need to specfiy all files that do not start with letters p or w or n,we use the argument [!pwn]* which indicates neither of the files which start with p or w or n as mentioned inside the [] which is a subset of wildcards.Hence when we run the final command,'/challenge/run [^pwn]*' we get the desired output ie.flag value.      
'''     
Connected!                                                                            
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files     
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*     
You got it! Here is your flag!      
pwn.college{4AogD_6R3i3sDwefEd2Vik_8KsR.QX2IDO0wCO1gjNzEzW}     
hacker@globbing~exclusionary-globbing:/challenge/files$      
'''     

## What I Learnt
I learnt the concept of exlcusionary globbing which involves the use of characters '!' or '^' which is used to specify the files that do not satisfy the globbing condition and show the rest.   

## References
None.     

<img width="608" height="95" alt="image" src="https://github.com/user-attachments/assets/e473cdc9-a70e-4831-8419-ce7cbab469f8" />
