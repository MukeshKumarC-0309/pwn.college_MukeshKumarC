# Extracting Specific Sections of Text
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'cut' command to get the desired output.     

## My Solve
**Flag:** 'pwn.college{8ra7cGdntkBT7X0c8w7Jn-7WjWx.01NxEzNxwCO1gjNzEzW}'   

Here,we are asked to get the flag from the '/challenge/run' file but when opened it has the flag all mixed up with the flag contents split by letters on each line after a random number.Hence to extract that column alone we use the 'cut' command which is used to remove specific parts text.We use the '-d' which stands for column delimiter that splits it up into columns.The argument to be passed is " " because the letters are seperated by a space,and we need the 2nd column.Hence we use 'cut -d  " " -f 2' to get that specific column and to show them in a single line we can use the 'tr -d' command to delete the newlines.Hence our final code ie.'/challenge/run | cut -d  " " -f 2 | tr -d "\n"' when run gives us the final output successfully.   
'''     
Connected!    
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run      
2813 p     
28380 w     
14923 n     
18232 .    
15656 c    
13031 o    
3141 l     
11706 l    
10702 e    
10501 g    
5956 e    
8213 {    
18469 8   
12683 r    
17516 a     
6838 7     
15115 c    
28432 G    
10576 d    
21452 n    
12035 t    
32261 k    
32729 B   
12584 T    
28561 7   
20345 X    
14326 0    
32474 c    
21824 8    
26126 w    
19117 7    
19728 J    
4517 n    
27672 -    
15721 7    
30644 W    
25340 j    
7834 W    
6642 x    
7343 .     
10989 0    
15194 1    
7125 N    
29851 x    
1792 E    
7966 z    
11257 N    
30183 x    
14883 w    
835 C    
13047 O    
31325 1    
6710 g     
2075 j     
22711 N     
5857 z    
12124 E    
32414 z    
22601 W     
12687 }                                                                             
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d  " " -f 2 | tr -d "\n"     
pwn.college{8ra7cGdntkBT7X0c8w7Jn-7WjWx.01NxEzNxwCO1gjNzEzW}hacker@data~extracting-specific-sections-of-text:~$     
'''    

## What I Learnt
I learnt the use of 'cut' command which is used to choose specific sections of the text using suitable delimiters and arguments.     

## References
None.    


<img width="671" height="17" alt="image" src="https://github.com/user-attachments/assets/089fe7a5-a8b0-48c9-a9e0-c51f2d645dfd" />     



<img width="702" height="898" alt="image" src="https://github.com/user-attachments/assets/d41ecea8-987f-4450-a28c-21c0b5387f51" />    



<img width="848" height="20" alt="image" src="https://github.com/user-attachments/assets/1560c02d-7b6f-4ad6-b640-861655a2440d" />



