# Learning From Documentation
The challenge asks you to open the terminal in the pwn.college DOJO and use arguements while opening a file to get desired output.  
## My Solve
**Flag:** 'pwn.college{A2JywXu83CYyFGezOZniXWa2l7R.QX0ITO0wCO1gjNzEzW}'  

Here we use the '/' command to open a certain file.But this time we are supposed to give a certain arguement(in this case '--giveflag') along with the '/challenge/challenge' command which works perfectly giving us the desired output.  
'''   
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag       
Correct argument! Here is your flag:      
pwn.college{A2JywXu83CYyFGezOZniXWa2l7R.QX0ITO0wCO1gjNzEzW}       
hacker@man~learning-from-documentation:~$       
'''      

## What I Learnt
We learnt that we can also pass arguements along with opening files to bypass certain limitations.  

## References
None.   


<img width="626" height="90" alt="image" src="https://github.com/user-attachments/assets/87285476-cbc6-4f26-b555-b98650beea54" />
