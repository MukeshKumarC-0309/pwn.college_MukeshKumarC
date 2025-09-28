# Reading Files
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'read' command to get the desired output.        

## My Solve
**Flag:** 'pwn.college{Y-qyqfY9tpc4YzwjnbEtCUBNPUT.QXwIDO0wCO1gjNzEzW}'         

Here,we are asked to read the command '/challenge/read_me' into a variable PWN.But it’s given that the '/challenge/read_me' keeps changing,so we have to complete the challenge in 1 step.Previously,we saw that the 'read' command can be used to read user inputs.Now,we see that it can also be used to read files into the shell using the input redirection ('<') along with the read command.Hence by using,'read PWN < /challenge/read_me' we tell the shell to redirect the output of '/challenge/read_me' to the variable 'PWN' in a single step.Hence,we successfully complete the challenge and we get the desired output(flag).   
'''    
Connected!                                                                           
hacker@variables~reading-files:~$ read PWN < /challenge/read_me     
You've set the PWN variable properly! As promised, here is the flag:      
pwn.college{Y-qyqfY9tpc4YzwjnbEtCUBNPUT.QXwIDO0wCO1gjNzEzW}         
hacker@variables~reading-files:~$      
'''     

## What I Learnt
I learnt that by combining the 'read' command with the '<' command which is used for input redirection,it is possible for us to read files into the shell also.   

## References
None.     

<img width="724" height="87" alt="image" src="https://github.com/user-attachments/assets/538603db-2a4a-4113-ba02-a57080038e6e" />

