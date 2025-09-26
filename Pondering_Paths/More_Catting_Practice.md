# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'cat' command with an aboslute file path as arguement to get desired output.
## My Solve
**Flag:** 'pwn.college{YbIJMi7WzezErky3YR9Y4-EtXpU.QXwITO0wCO1gjNzEzW}'   

In this challenge,we are asked to run the '/flag' command but we are restricted to only giving the absolute file path as the arguement.Usage of 'cd' command was banned and we aren’t allowed to switch between directories.Hence with the help of given file location,we use the 'cat' command with the absolute file path as the arguement which gave us the desired output.  
'''   
hacker@commands~more-catting-practice:~$ cat /usr/include/rdma/flag     
pwn.college{YbIJMi7WzezErky3YR9Y4-EtXpU.QXwITO0wCO1gjNzEzW}     
hacker@commands~more-catting-practice:~$     
'''     

## What I learnt
I learnt that in addition to file name and relative file paths,'cat' command can also take absolute file paths as an arguement which can be used to read files which are in different directories.  

## References
None.    


<img width="540" height="102" alt="image" src="https://github.com/user-attachments/assets/272c2223-f8d9-497d-9291-0648c6317b62" />
