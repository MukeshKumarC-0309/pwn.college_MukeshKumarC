# Filtering with grep -v
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'grep' command with an invert match to obtain the desired result.      

## My Solve
**Flag:** 'pwn.college{kCy40nr3UitmZTmTFrtRWXjU0mq.0FOxEzNxwCO1gjNzEzW}'       

Here,we are asked to run the command '/challenge/run' and find the right flag.But there are thousands of decoy flags and finding the right one is very time consuming.Hence we can use an ivert match that can avoid results that contain a certain phrase which is passes as argument.Hence if we run 'grep -v hell' for example,it will print all the results which don’t have the phrase 'hell' in them.So here,it’s given that all the decoy flags contain the word 'DECOY'.Hence to avoid them,we can use 'grep -v DECOY' to filter out the right flag.Hence our final command,'/challenge/run|grep -v DECOY' when run gives us the final output ie.flag value.    
'''    
hacker@piping~filtering-with-grep-v:~$ /challenge/run|grep -v DECOY      
pwn.college{kCy40nr3UitmZTmTFrtRWXjU0mq.0FOxEzNxwCO1gjNzEzW}     
hacker@piping~filtering-with-grep-v:~$      
'''     

## What I Learnt
I learnt the usage of invert match ie.'-v' command which can be used to filter out the text that contain a certain phrase given as argument which makes searching files much less cumbersome.    

## References
None.     

<img width="517" height="54" alt="image" src="https://github.com/user-attachments/assets/3112afb3-8707-4f75-84f6-adea7ee4caeb" />


