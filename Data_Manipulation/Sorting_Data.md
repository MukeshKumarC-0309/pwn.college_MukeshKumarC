# Sorting Data
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'sort' command to get the desired output.    

## My Solve
**Flag:** 'pwn.college{sWSP74_rBV67c5Ng4uqPLmDJjti.0FM0MDOxwCO1gjNzEzW}'       

Here,we are asked to find out the real flag from the bag of mixed flags in '/challenge/flags.txt'.But we know that when sorted alphabetically,the real flag is present in the end.Hence we can use the 'sort' command to get the flag.The 'sort' command is used to sort the lines in the text in alphabetical order or in any order specified by arguments.Hence when we run 'sort /challenge/flags.txt' we get the entire file in alphabetical order and we can find the right flag at the end of the file.     
'''       
Connected!                                                                           
hacker@data~sorting-data:~$ sort /challenge/flags.txt    
ovm.bnlkefe{rWSP74_rAU67b4Nf4uqPLlCIjsi.0EL0LDOxwCO0gjNzEzW}    
ovm.bnllegd{rWRP64_rBV57c5Ng4tqPKlDJjti.0FM0MDNxvCO1gjNzEyW}    
ovm.college{sWRP73_qAU66c4Ng4upPKmCIisi.0EM0MDOxwCO1gjMzDyW}    
ovn.bnllege{sWSP74_qBV66c4Ng4uqPLmDJjti.0FM0MCOxwCO1gjNzEzV}     
ovn.cnkldge{sWRP64_rBU67b5Ng4uqOKmCJjsi.0FM0MCOxwCO1fjNzDzW}     
ovn.cokldgd{sWRP73_rAV67c4Mg4tpPLmDJjth.0FM0MDOxvCO1giMzDyV}    
ovn.cokldge{sWRP74_rBU67c5Mf4upPLlDJith.0FM0LDOwwCO1gjNzEzW}    
ovn.coklefe{rWSO74_qBV57c4Mf4tqPLlDIjsi.0EM0LDNxvBO1giNyEzW}     
owm.bolkege{sVSO74_rAV67c4Ng3uqPLmDJjth.0FM0LDOxwBN0gjNyEyW}     
owm.cnklegd{sWSP64_qBV66c5Ng4tqPKmCIjth.0EL0MDOwwCO0gjNyDzW}    
owm.cokkefe{rWSP73_qBV67b4Mg4upPLmDJiti.0FM0MDOwwCO0fiNzDzW}      
own.bolkegd{sWSP73_rBV67b4Nf4upOLmCJjsi.0FM0MDNxwCN0gjNyEzW}      
own.bolldge{sWSO73_qBV67c4Ng4tqPLmDJjsi.0EL0MCOwwCN1gjNzEzV}    
own.bollefe{rVSP74_rAV67c5Ng4uqPLmDJisi.0FM0MDOxwCO1gjNzDyW}    
own.cokkege{rWSO73_rBU66c5Mg3uqOKmDJjth.0FM0LDOxvCO1fiNzDzV}    
own.coklege{sWSP74_qBV67c5Ng3tqPKlDJjth.0EM0LDOxwCN1gjNyEyW}    
own.coklege{sWSP74_rBV67c5Ng4uqOLmDJjti.0FM0MDNxwCO1gjMzDzW}     
own.colldge{sWSP74_rBV67c5Mf4tqPLmCJjti.0EM0MDOxvCO1gjNzEzV}     
own.collefe{sWRP64_qAV67c5Mf4upOKlDJjth.0FM0MDOxwCN1gjNyEzW}        
own.collegd{sVRP74_rBV67c5Mg4uqPLlDIjth.0EM0MCOwwCO1giNzEyW}      
pvm.bolldge{sWRP74_rBV67c5Ng4uqOLmDJjti.0FM0LCOxwCO0gjNzEzV}     
pvm.bollege{rWSP73_rBV57b5Ng4uqPKlDJith.0FL0MCNxwBO1fjMzDzV}     
pvm.cnlkege{rWRP74_rBU56c5Mg4tqPLmCIiti.0FL0LDNwwCO1gjNzEyV}     
pvm.college{sWSP74_qBV67c4Nf4uqPLlDIjth.0FL0LDOxwBN1giMzEzV}     
pvn.bokldgd{sWSP74_qBV57c4Ng3uqPLmDJjsi.0FL0MDOwvCO1giNzEzW}     
pvn.bolkdge{sWRP64_rAV66b4Ng4upPLmDJjsi.0FM0LDOxvBO0giNzEzW}     
pvn.bolldfd{rWSP74_rBU57c5Ng3tqPLlDIith.0FL0LCOxwCO0fjNzEzV}     
pvn.bollege{rWSP73_qAV66c4Nf4uqOLlCJjsi.0EM0MDOxwBO1giNyDyW}    
pvn.cnkkefe{rWSP64_rBV67c5Ng4uqPLmDJisi.0FL0LDOwwBN1gjNzEzV}    
pvn.cnklege{sWSP74_rBU67c5Ng3tqPLmDJjti.0FM0MDOxwBO1gjNzEzW}    
pvn.cnllege{sVSO73_rAV56c5Ng4tqPLmDIjti.0FL0MDOxwBO1gjMzEzV}    
pvn.colkdge{rWSP73_rAU56b5Ng3upPLmCJjsi.0EM0LDNxwCO1giMzDzW}     
pvn.colldgd{sWSP74_rBV67c5Ng4tqPKmDJith.0FM0MDOxwCO1gjNzEzW}    
pvn.collegd{sVSO73_qAV66c5Ng4tqPLmDJiti.0FL0LCOxwBO0fjNyEyW}    
pvn.college{rWSP63_qBV67c4Mg4uqPLmDJjti.0FL0MDNwwCN1fiNyDzW}    
pvn.college{sWRP73_rBU67c5Nf4tqPLmDJiti.0FM0MCNwwCO1fiNzEyW}    
pwm.bnllefe{sWRP64_qBV57c5Nf3upPKlCIiti.0FM0MDOxwCN1gjMyEzW}    
pwm.bnllegd{sWRO73_rBV57c5Ng4uqOLmCJiti.0FM0LDOwwCN0fjNzEzW}    
pwm.boklege{sWRP74_rBV57c5Ng4tqPLlDIiti.0FM0MCOwvCN1gjNzEzV}    
pwm.bolkefe{sWRP74_rBV66c5Ng4uqPLmDIjti.0EM0MDOxvCO0gjNzEzW}        
pwm.bolldge{sWSP74_rBU67c5Mg4upOLlDJisi.0EM0MDOxwCO0gjNzDzW}        
pwm.cnklege{sWRO74_rBV67c5Ng4upPLmCIith.0EM0MCOwvBO1fiNzEzW}    
pwm.cnlldge{sWSP73_rBV67c5Ng3tqOKmDJjti.0FM0MDOxwCO1fiNzDzV}    
pwm.coklege{sWSO74_qBU66c5Mg4uqPLmCJjth.0EL0MCNwwBO0fjNyEzV}    
pwm.colldfe{rWSP73_rBV67c5Ng4tpPKlCJiti.0FM0MCOxwCO1gjNzEzW}    
pwm.collefe{rWSP63_qBV66b5Mg4tqOLlDIjti.0FM0MDNxwCN1gjNzEzV}    
pwm.collegd{sWSP74_rBV67b5Ng4uqPLlDJiti.0FM0MDOxvCO1gjNzEzW}   
pwm.college{rVSP74_rBU67b5Ng4uqPLmCIjti.0EM0LDOxwBN0gjNzEzW}    
pwm.college{sVRP73_rBV67c4Ng4upOLmDJjti.0FM0MDOxwCO1gjNzEzW}   
pwm.college{sVSP74_rBV56b5Ng4uqPLlDJjti.0FM0MDOxwCO0giNzEzV}   
pwm.college{sWRP64_rAU66c5Nf4uqPKmCJjsi.0EM0LCOwvCN1fiNyDyW}    
pwn.bnlldgd{sWSP74_rBV66c5Ng4upPLmDIjsi.0FM0MCNxvCO1giNzEzV}    
pwn.bnlldge{sWSP63_qBV57b5Nf4uqPLlCIjti.0EM0LCOxwBN1gjNyEyW}     
pwn.bokldgd{sWSP64_rBV66c5Mg4uqPLlCIjti.0EM0MDNxwCO0gjNzDzW}     
pwn.bolkege{sWRP73_qBU67c5Ng4upPKmCIjti.0FM0MCOxwCO1gjMzEzW}           
pwn.bolkege{sWSO74_rBV67c4Ng3tqPLlCJjth.0EL0MCOxwCN1fjNyDyW}      
pwn.bolldfe{sVSP73_rAU67c5Mg4upPLlCJjsi.0EM0MDOwwCO1fjNzEzW}       
pwn.bollege{sVSP74_rBV67c4Ng4uqPLmDJjti.0FM0MDOxwCO1fjNzEzW}     
pwn.cnklefe{sWRO74_rBV57c5Mf4uqPKmDIjsi.0EL0MDOwwCO1gjMyEzW}    
pwn.cnlldge{sVSP74_rBV66c5Ng3uqPLlCJiti.0FM0MDOxvCO0fjNyEyW}   
pwn.cnllegd{sWSP74_rBV67b5Ng4upPLmDJjti.0FM0MDOxwCO1gjNzEzW}    
pwn.cnllege{sVSO74_rBV67c5Ng3upPKmDJjti.0FM0MCOxwCO0giNzEzW}    
pwn.cokldge{sVSP74_rBU67c5Ng4uqPLmDJjsi.0FL0MDOxwCO1fjNzEzW}    
pwn.coklefd{sWRP74_qBV66c5Ng4tqPKlDJjti.0FM0MDOxwCO1fjMyEzW}    
pwn.coklefe{rWSO64_rAV67c5Ng4uqPLmDJisi.0FM0LDNwwCO0giNzEzV}    
pwn.coklege{sWSO74_rBV57c5Ng3uqPLmDJjti.0FM0MDOxwCO1gjNzEzW}    
pwn.coklege{sWSP64_rBU67c5Ng3uqPLmDJjti.0FM0MDOxwCO1gjNyEzW}    
pwn.colkegd{sWSO74_rAV66c5Ng4upOLlDIjti.0EL0MCOxwCO0gjNzEzW}    
pwn.colkege{sWSO73_rBV66c4Ng4uqOLmDJjti.0FM0MCOwwBO1fjNzEzV}    
pwn.colkege{sWSP74_rBV67b5Mg4uqPLmDJjti.0FM0MDOxwCO1gjNzEzW}    
pwn.colldge{rWSO74_rBV66b5Nf4uqPLmDJjti.0FM0MDOxwCO1gjNzDzW}   
pwn.colldge{rWSP73_rBV66c4Mg4tqOLmDJisi.0FM0LCOxvBO0gjMzEzW}   
pwn.colldge{sWSP74_rBV67c5Ng4tqPLlCJjti.0FM0MDOxvCO1giNzEzW}   
pwn.collefd{rVSP73_rBV66c5Nf4uqPLmDJjsi.0FM0MDOxvCO1fjMzEzW}        
pwn.collefe{sVSP74_rBV67c5Mf4uqOLmDJjsi.0EM0MDNwwCO0fjNzDyV}    
pwn.collefe{sWSP74_rBV67c5Ng4uqPLmDJjti.0FM0MDOxwCO1gjNzEzV}    
pwn.college{rWRP73_rBV57c4Mg4upPLmDJjsi.0FL0MDNxwCN1gjNzEzW}    
pwn.college{sVRP74_rAV57c4Ng4upOLlDJjti.0FM0MDOxwCO0gjNyEzW}    
pwn.college{sVSP74_rBU67b5Ng4uqPKlDJjth.0FM0LDOxwCO0fjNzDyW}    
pwn.college{sWRP73_rBV67c5Ng4uqPKmDJjti.0FM0LDOxwCN1gjNzEzW}    
pwn.college{sWRP74_rBV67c5Ng4upPLmDJjti.0FM0MDOxwCO1gjNzEyW}    
pwn.college{sWRP74_rBV67c5Ng4uqPLmDJjti.0EM0MDOxwCO1gjNzEzW}   
pwn.college{sWSO74_rBV67c5Nf3upPKmCJjti.0FM0MDOxvCO1gjNzEzW}    
pwn.college{sWSP74_qBV66c5Ng4uqPKmDJjti.0FL0MDOxwCO1gjNzEzW}     
pwn.college{sWSP74_qBV67c5Ng4uqPLmCIjti.0FM0MDOxwCO1gjNzEzW}     
pwn.college{sWSP74_rAV57b5Ng3tpOLmDJjsi.0FL0LDOxwCO1gjMzDzW}    
pwn.college{sWSP74_rBV57c5Ng4uqPLmDJiti.0FM0MDOxwCO1gjNzEzW}    
pwn.college{sWSP74_rBV66c5Nf4uqPKmDJjti.0FM0MDOxwCO1gjNzEzV}    
pwn.college{sWSP74_rBV66c5Ng4tqPLmDJjti.0FM0MDOwwCO1gjNzEzW}    
pwn.college{sWSP74_rBV67b5Ng4uqPLmDIjti.0FM0MDOxwCN1gjNzEzW}   
pwn.college{sWSP74_rBV67b5Ng4uqPLmDJjti.0FM0MDOxvCO1gjNzEzW}    
pwn.college{sWSP74_rBV67c4Ng4uqPLmDJjti.0FM0MDOxwCO1giNzDzW}    
pwn.college{sWSP74_rBV67c5Ng4upPKmDJjti.0FM0MDNxwCO1fjNzEzV}    
pwn.college{sWSP74_rBV67c5Ng4upPLmDJjti.0FM0MDOxwCO1gjNzEyW}    
pwn.college{sWSP74_rBV67c5Ng4uqPLlDJjti.0FM0MDOxwCO1gjNzEzW}    
pwn.college{sWSP74_rBV67c5Ng4uqPLmDJjsi.0FM0MDOxwCO1gjNzEzW}    
pwn.college{sWSP74_rBV67c5Ng4uqPLmDJjti.0EM0MDOxwCO1gjNzEzW}    
pwn.college{sWSP74_rBV67c5Ng4uqPLmDJjti.0FM0MCOxwCO1gjNzEzW}    
pwn.college{sWSP74_rBV67c5Ng4uqPLmDJjti.0FM0MCOxwCO1gjNzEzW}    
pwn.college{sWSP74_rBV67c5Ng4uqPLmDJjti.0FM0MDOxwCO1gjNzDzW}    
pwn.college{sWSP74_rBV67c5Ng4uqPLmDJjti.0FM0MDOxwCO1gjNzEzW}   
hacker@data~sorting-data:~$      
'''     

## What I Learnt
I learnt the usage of the 'sort' command which can be used to sort the text in the file in alphabetical order or in any other order according to the argument specified in the terminal.      


## References
None.   



<img width="511" height="899" alt="image" src="https://github.com/user-attachments/assets/01e35eba-ac8b-4bbe-8bd5-066a120dfb58" />     




<img width="511" height="618" alt="image" src="https://github.com/user-attachments/assets/8207596b-1094-4a7c-b053-616d7f03e481" />


