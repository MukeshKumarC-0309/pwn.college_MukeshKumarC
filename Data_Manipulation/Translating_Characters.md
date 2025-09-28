# Translating Characters
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'tr' command to get desired output.     

## My Solve
**Flag:** 'pwn.college{MOjL-jUTSKSWHv-5Ud21nEW0TIp.01MxEzNxwCO1gjNzEzW}'    

Here,we are asked to find the correct flag value since all the cases are flipped.Hence the 'tr' command comes in use here.The 'tr' command is used to translate from 1 character to another given in argument.Here we must convert lowercase to upper case and vice versa.Hence we use "tr '[ABCDEFGHIJKLMNOPQRSTUVWXYZ][abcdefghijklmnopqrstuvwxyz]' '[abcdefghijklmnopqrstuvwxyz][ABCDEFGHIJKLMNOPQRSTUVWXYZ]'" where ' ' are used to avoid shell interpretation and [] is used to have a set of potential wildcards.Here,uppercase becomes lowercase and vice versa.Hence our final command ie."/challenge/run | tr '[ABCDEFGHIJKLMNOPQRSTUVWXYZ][abcdefghijklmnopqrstuvwxyz]' '[abcdefghijklmnopqrstuvwxyz][ABCDEFGHIJKLMNOPQRSTUVWXYZ]'" gives us the final output(flag).   
'''    
Connected!                                                                                
hacker@data~translating-characters:~$ /challenge/run | tr '[ABCDEFGHIJKLMNOPQRSTUVWXYZ][abcdefghijklmnopqrstuvwxyz]' '[abcdefghijklmnopqrstuvwxyz][ABCDEFGHIJKLMNOPQRSTUVWXYZ]'        
yOUR CASE-SWAPPED FLAG:     
pwn.college{MOjL-jUTSKSWHv-5Ud21nEW0TIp.01MxEzNxwCO1gjNzEzW}      
     
hacker@data~translating-characters:~$     
'''     

## What I Learnt
I learnt the use of 'tr' command which helps translate from 1 character to another which are given as arguments in the terminal.    

## References
None.     

<img width="1249" height="87" alt="image" src="https://github.com/user-attachments/assets/f3b0abc1-aa82-4e7a-bd1e-5530735bd814" />


