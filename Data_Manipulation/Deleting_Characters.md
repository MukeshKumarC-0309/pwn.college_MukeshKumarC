# Deleting Characters
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'tr -d' command to get the desired output.    

## My Solve
**Flag:** 'pwn.college{Qx_niNPsHVEQRvbKjkU96mA_B_m.0FNxEzNxwCO1gjNzEzW}'    

Here,we are asked to remove certain elements from the flag to get the original value.We know that the 'tr' command is used to translate characters.To remove the characters we use the 'tr' command along with the '-d' prompt which helps delete all occurances of the characters given as argument.Here,the extra characters are '^' and '%' respectively.Hence if we give them as argument to the 'tr -d' command,it will remove all occurances of that character.Hence on running "/challenge/run | tr -d ^%" we get the final flag output.   
'''    
Connected!                                                                           
hacker@data~deleting-characters:~$ /challenge/run | tr -d ^%    
Your character-stuffed flag:     
pwn.college{Qx_niNPsHVEQRvbKjkU96mA_B_m.0FNxEzNxwCO1gjNzEzW}     
hacker@data~deleting-characters:~$     
'''     

## What I Learnt
I learnt the use of the 'tr -d' command which is used to delete all occurances of a character passed as argument to filter out the unwanted characters in a file.    

## References
None.    

<img width="690" height="87" alt="image" src="https://github.com/user-attachments/assets/e51f7f61-0a40-410e-b206-2cc6484b7415" />
