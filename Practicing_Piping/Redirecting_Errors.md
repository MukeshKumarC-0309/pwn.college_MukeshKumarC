# Redirecting Errors
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the '>' command to get desired output.       

## My Solve
**Flag:** 'pwn.college{cejQnUfzmCzwFnfdbEM-Fj6FLp0.QX3YTN0wCO1gjNzEzW}'     

Here we are asked to use the '>' command to redirect files in the terminal.Here we use the '>' command to redirect the file '/challenge/run' to a new location 'myflag' and simulatenously redirect the errors(int this case instructions) to a new location 'instructions'.So we use the '>' command twice,one to shift the file and the other to shift the error.Hence our command looks like '/challenge/run > myflag 2>instructions' where '2' stands for stderror.By running the command,we get the desired flag.     
'''    
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2>instructions      
hacker@piping~redirecting-errors:~$ cat myflag     
      
[FLAG] Here is your flag:     
[FLAG] pwn.college{cejQnUfzmCzwFnfdbEM-Fj6FLp0.QX3YTN0wCO1gjNzEzW}     
     
hacker@piping~redirecting-errors:~$      
'''     

## What I Learnt
I learnt that other than redirecting files and text,we can also use the '>' command to redirect errors to a new location in order to avoid certain situations.   

## References
None.     


<img width="654" height="112" alt="image" src="https://github.com/user-attachments/assets/4acd7a92-3874-498a-9754-89b210b3526f" />

