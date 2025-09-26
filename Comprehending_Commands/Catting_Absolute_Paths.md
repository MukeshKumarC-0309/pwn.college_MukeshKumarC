# Intro To Arguments
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'cat' command with a file path as arguement to get the desired output.   

## My Solve
**Flag:** 'pwn.college{EWPDnBl65EXQgY2VEPO9MlSSjif.QX5ETO0wCO1gjNzEzW}'    

Here,we use the 'cat' command with a file path as the arguement.We learn that 'cat' command can also take file paths as an arguement,as shown here.Here we specify the file path '/flag' as the arguement which reads the file 'flag' giving us the desired output.  

'''   
hacker@commands~catting-absolute-paths:~$ cat /flag    
pwn.college{EWPDnBl65EXQgY2VEPO9MlSSjif.QX5ETO0wCO1gjNzEzW}    
hacker@commands~catting-absolute-paths:~$     
'''   

## What I learnt
I learnt that in addition to mentioning file names as the arguement in the 'cat' command,we can also specify file paths as the arguement in order to traverse through directories to find the desired file.  

## References
None.    

<img width="540" height="54" alt="image" src="https://github.com/user-attachments/assets/7788f898-f830-4790-a44c-21363dec3495" />
