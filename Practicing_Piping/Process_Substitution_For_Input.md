# Process Substitution for inputs
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'diff' command to get the desired output.   

## My Solve
**Flag:** 'pwn.college{4Lh23Q9p5D0hXUnIoguq2Nv0Nd4.0lNwMDOxwCO1gjNzEzW}'    

Here,we are asked to use the 'diff' command to compare two outputs '/challenge/print_decoys' and '/challenge/print_decoys_and_flag' to find the real flag.Hence we use process subsitution to connect both outputs.It involves the use of the '<' command to create a redirection of outputs.Hence when we run 'diff -- <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)' it shows the first instance where there's a chance,ie.93a94(after line 93 of file 1 add line 94 of file 2) which gives us the flag output.   
'''    
hacker@piping~process-substitution-for-input:~$ diff -- <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)      
93a94      
> pwn.college{4Lh23Q9p5D0hXUnIoguq2Nv0Nd4.0lNwMDOxwCO1gjNzEzW}      
hacker@piping~process-substitution-for-input:~$
'''

## What I Learnt
I learnt process substitution which involves the '<' command which is used to hook the input/output of programs to a argument of commands.     

## References 
None.     


<img width="915" height="72" alt="image" src="https://github.com/user-attachments/assets/303de5af-aed6-44e0-bd8e-692e113b71c3" />
