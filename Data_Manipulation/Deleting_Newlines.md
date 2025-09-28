# Deleting Newlines
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'tr -d' command to get the desired output.   

## My Solve
**Flag:** 'pwn.college{YCW_oSx_Ee1sFhn1plnZOBd4LV1.0VNxEzNxwCO1gjNzEzW'      

Here,we are asked to remove all the newlines in the file such that we get the desired flag output.Like the previous challenge we can use the 'tr -d' command to delete all the newlines.Newlines are denoted by "/n".Hence if we pass 'tr -d "/n"' it would delete all the newlines.Hence our final command ie.'/challenge/run | tr -d "\n"' runs successfully and gives us the final flag output.    
'''     
Connected!                                                                              
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"       
Your line-split flag: pwn.college{YCW_oSx_Ee1sFhn1plnZOBd4LV1.0VNxEzNxwCO1gjNzEzW}hacker@data~deleting-newlines:~$      
'''     

## What I Learnt
I learnt further usage of the 'tr -d' command as it can be used to delete newlines also if given correctly as the argument.    

## References
None.    

<img width="844" height="59" alt="image" src="https://github.com/user-attachments/assets/00a9f599-cdd1-411a-aeb2-b6af34f8cb37" />
