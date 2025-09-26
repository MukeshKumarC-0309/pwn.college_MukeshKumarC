# Multiple Options for Tab Completion
The challenge asks you to open the terminal in the pwn.college DOJO and use the 'tab' key for multiple similar files to get the desired output.     

## My Solve
**Flag:** 'pwn.college{E6RyHmPmQRdew1jSZ3EdMKT8XW3.0lN0EzNxwCO1gjNzEzW}'        

Here,we are asked to use the 'tab' key to autocomplete the command(file path).But this time there are multiple files with similar options.So when we first click tab,it autocompletes till the point where all files are different,and clicking tab again it shows us the list of all available options.Then after giving the next letter and clicking tab,the whole process restarts again.Hence,in this scenario we see the after typing 'cat /challenge/files/pwncollege-' using tab key,we find the suitable file,more specifically the 'flag' file.Hence,we run the command 'cat /challenge/files/pwncollege-flag',we get the desired output.   
'''     
Connected!                                                                             
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-    
pwncollege-family      pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter  pwncollege-hacking        
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag     
pwn.college{E6RyHmPmQRdew1jSZ3EdMKT8XW3.0lN0EzNxwCO1gjNzEzW}     
hacker@globbing~multiple-options-for-tab-completion:~$      
'''     

## What I Learnt
I learnt that when multiple files are present with similar letters,we can use the tab space systematically to slowly filter out the unwanted files and pick the right one by autocompleting the path part by part.    

## References
None.   

<img width="784" height="97" alt="image" src="https://github.com/user-attachments/assets/bf1bc573-0e9a-4961-a14c-afbbea4648ce" />
