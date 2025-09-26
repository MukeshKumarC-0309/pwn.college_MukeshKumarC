# Explicit Relative Path
The challenge asks you to open the terminal in the pwn.college DOJO and use the './' commands to explicity specify the path to get the desired flag.     

## My Solve
**Flag:** 'pwn.college{Y60C0rVkAZTh9iwp_9l6F-CZHLw.QXwUTN0wCO1gjNzEzW}'   

First,we start by using the '/challenge/run' command to invoke the flag,but we get an unexpected error stating that we are in the wrong directory and asks us to change to the '/' directory.Hence we use the 'cd' command to change to the said directory.After that,we invoke the flag by using the './challenge/run' command as we are instructed to explicitly invoke the file path,by doing so we get the desired output flag.  

'''    
hacker@paths~explicit-relative-paths-from-:~$ /challenge/run      
Incorrect...     
You are not currently in the / directory.     
Please use the `cd` utility to change directory appropriately.       
hacker@paths~explicit-relative-paths-from-:~$ cd /       
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run       
Correct!!!       
./challenge/run is a relative path, invoked from the right directory!      
Here is your flag:      
pwn.college{Y60C0rVkAZTh9iwp_9l6F-CZHLw.QXwUTN0wCO1gjNzEzW}       
hacker@paths~explicit-relative-paths-from-:/$       
'''   

## What I learnt
I learnt that there's another method of invoking files ie. the explicit method which involves the use of '. or ..' commands along with the relative path which can be used to traverse through directories.       

## References
None.       

<img width="985" height="162" alt="image" src="https://github.com/user-attachments/assets/145bfee1-45b9-4999-97f7-b587d4f8a289" />

