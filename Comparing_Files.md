# Comparing Files
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'diff' command to compare 2 files to get the output.     

## My Solve
**Flag:** 'pwn.college{U-1XWlQw1P-vIZ-Xjxu44mPm0kv.01MwMDOxwCO1gjNzEzW}'    

First we use the 'cat' command for the 2 files given and we see that both files have a lot of decoy flags and manually filtering them out would be impossible.Hence we use the 'diff' command that's used to compare files and mention the instance wherein there's a difference between the two files,in this case the ouput is '62a63' which means 'after line 62 of file 1,add line 63 of file 2' which indicates that there's only one line different in both files,which is in turn the real flag,thereby getting the desired output.  
'''  
hacker@commands~comparing-files:~$ cat /challenge/decoys_only.txt   
pwn.college{fake_flag_number_1_dfNQ68bjazU}    
pwn.college{fake_flag_number_2_GN25kE5GyMk}    
pwn.college{fake_flag_number_3_DNOMuZMH2I}     
pwn.college{fake_flag_number_4_tepTlbo74gM}    
pwn.college{fake_flag_number_5_IO4VqhCsoVg}    
pwn.college{fake_flag_number_6_fmrOEHqEdu8}     
pwn.college{fake_flag_number_7_pyjk6GDuJQ}     
pwn.college{fake_flag_number_8_Tm0YB4SbyY}    
pwn.college{fake_flag_number_9_aBNOHZWr8fE}    
pwn.college{fake_flag_number_10_bSSKUOMAww}   
pwn.college{fake_flag_number_11_50JjwoS6Tn4}   
pwn.college{fake_flag_number_12_HspCCucljOc}   
pwn.college{fake_flag_number_13_3j5BXnUYrQ}   
pwn.college{fake_flag_number_14_Hm6jtaqRDOo}   
pwn.college{fake_flag_number_15_vflD4830E8Q}   
pwn.college{fake_flag_number_16_imE2E7VwKBM}   
pwn.college{fake_flag_number_17_ADC3aneyvI8}   
pwn.college{fake_flag_number_18_IfuP9McmykI}    
pwn.college{fake_flag_number_19_IfcUBRtIDBI}   
pwn.college{fake_flag_number_20_n8vOLQC2GRU}   
pwn.college{fake_flag_number_21_7buHybJ18mw}   
pwn.college{fake_flag_number_22_4wFPZ4jM5g}   
pwn.college{fake_flag_number_23_vECu2CcIO3A}      
pwn.college{fake_flag_number_24_MmBxTHNl67M}   
pwn.college{fake_flag_number_25_A7xoi8oFnYA}   
pwn.college{fake_flag_number_26_rLBeNjAW2qE}   
pwn.college{fake_flag_number_27_z3Pmkuu10Tk}   
pwn.college{fake_flag_number_28_rc0iYxOlMC4}    
pwn.college{fake_flag_number_29_Rnuvs8UVtAw}   
pwn.college{fake_flag_number_30_68hkucr2So}   
pwn.college{fake_flag_number_31_rRO6JtIZiw}   
pwn.college{fake_flag_number_32_pW2w8KdrXk}   
pwn.college{fake_flag_number_33_1ncMF9QqzdU}   
pwn.college{fake_flag_number_34_9n1VmpzoyOc}   
pwn.college{fake_flag_number_35_owUtidHJqzA}    
pwn.college{fake_flag_number_36_x04E5PSaoas}    
pwn.college{fake_flag_number_37_sLSD8hLw9XM}    
pwn.college{fake_flag_number_38_UnSbX8YefmM}    
pwn.college{fake_flag_number_39_Zt2YZyT9U3M}  
pwn.college{fake_flag_number_40_tszrLnne0}   
pwn.college{fake_flag_number_41_TCmA1DYiuA0}    
pwn.college{fake_flag_number_42_5RTCevHZPuY}    
pwn.college{fake_flag_number_43_8a6Z2p646Mg}    
pwn.college{fake_flag_number_44_IdOSQCKHm70}    
pwn.college{fake_flag_number_45_0SabXjyNwI}    
pwn.college{fake_flag_number_46_1vcC6NnEifI}    
pwn.college{fake_flag_number_47_AgRIrya4Axs}   
pwn.college{fake_flag_number_48_bWfrjEDlmgY}  
pwn.college{fake_flag_number_49_n2PbjtEHerk}   
pwn.college{fake_flag_number_50_CnQe5bF3k}   
pwn.college{fake_flag_number_51_Wc6KDFl84}   
pwn.college{fake_flag_number_52_cWIZsgS488c}   
pwn.college{fake_flag_number_53_GoKPDILedo}   
pwn.college{fake_flag_number_54_as3ltngKkxM}   
pwn.college{fake_flag_number_55_DEQtdDIEC8w}   
pwn.college{fake_flag_number_56_fJFT3NHBuw}   
pwn.college{fake_flag_number_57_qApRH9149CY}      
pwn.college{fake_flag_number_58_b5iKsafXw4Y}    
pwn.college{fake_flag_number_59_MXlUV1lsm7E}  
pwn.college{fake_flag_number_60_khXtHkbd9gI}   
pwn.college{fake_flag_number_61_QaD2fhPxZw}   
pwn.college{fake_flag_number_62_TDvaXtAxJWg}   
pwn.college{fake_flag_number_63_4qvM6iw3MOQ}   
pwn.college{fake_flag_number_64_0K0wsy4wBIQ}   
pwn.college{fake_flag_number_65_MEeoPcokMI}   
pwn.college{fake_flag_number_66_tGzy6Zx0Jmo}   
pwn.college{fake_flag_number_67_9W7bBc6vi9w}   
pwn.college{fake_flag_number_68_cNNxeQlVyec}   
pwn.college{fake_flag_number_69_XUHmCkIR5g}   
pwn.college{fake_flag_number_70_EG8mPU5zj3o}   
pwn.college{fake_flag_number_71_UTNQFRhpvi8}   
pwn.college{fake_flag_number_72_JrYQTgKeDnU}    
pwn.college{fake_flag_number_73_9Y6VAXqAVs}  
pwn.college{fake_flag_number_74_8qTituVTWg}  
pwn.college{fake_flag_number_75_QGYxxHeNp5M}   
pwn.college{fake_flag_number_76_HQis4Dksppo}   
pwn.college{fake_flag_number_77_aGCRKJWG3zg}   
pwn.college{fake_flag_number_78_DvxXwEFgTaY}  
pwn.college{fake_flag_number_79_Kj3gjyThcRw}   
pwn.college{fake_flag_number_80_BRIc1UXHtIs}   
pwn.college{fake_flag_number_81_L3AQyR2VysM}   
pwn.college{fake_flag_number_82_XxnyBi5J6pA}   
pwn.college{fake_flag_number_83_jBBt1LaIyo}   
pwn.college{fake_flag_number_84_KUDX9WLllvM}   
pwn.college{fake_flag_number_85_9RxiEjOzTIQ}   
pwn.college{fake_flag_number_86_xVAt6K9ROz4}   
pwn.college{fake_flag_number_87_VwlzJFTSGlw}  
pwn.college{fake_flag_number_88_P4aKidRvUGM}  
pwn.college{fake_flag_number_89_Zy8ltGfenoM}  
pwn.college{fake_flag_number_90_6XohhjdfqM}  
pwn.college{fake_flag_number_91_2wDeGhK6Kg}  
pwn.college{fake_flag_number_92_9WtaaXY4ArU}  
pwn.college{fake_flag_number_93_wXr8jLljGA}  
pwn.college{fake_flag_number_94_zyYzPh2QauE}  
pwn.college{fake_flag_number_95_VF5XcAppnM}  
pwn.college{fake_flag_number_96_uBoebRRljpg}  
pwn.college{fake_flag_number_97_PUszhX3UbE}  
pwn.college{fake_flag_number_98_GLSkETo3gA}  
pwn.college{fake_flag_number_99_N3JPrDN00SY}  
pwn.college{fake_flag_number_100_qwEMyf499Y}  
hacker@commands~comparing-files:~$ cat /challenge/decoys_and_real.txt  
pwn.college{fake_flag_number_1_dfNQ68bjazU}   
pwn.college{fake_flag_number_2_GN25kE5GyMk}   
pwn.college{fake_flag_number_3_DNOMuZMH2I}   
pwn.college{fake_flag_number_4_tepTlbo74gM}   
pwn.college{fake_flag_number_5_IO4VqhCsoVg}   
pwn.college{fake_flag_number_6_fmrOEHqEdu8}   
pwn.college{fake_flag_number_7_pyjk6GDuJQ}   
pwn.college{fake_flag_number_8_Tm0YB4SbyY}   
pwn.college{fake_flag_number_9_aBNOHZWr8fE}   
pwn.college{fake_flag_number_10_bSSKUOMAww}   
pwn.college{fake_flag_number_11_50JjwoS6Tn4}   
pwn.college{fake_flag_number_12_HspCCucljOc}   
pwn.college{fake_flag_number_13_3j5BXnUYrQ}   
pwn.college{fake_flag_number_14_Hm6jtaqRDOo}   
pwn.college{fake_flag_number_15_vflD4830E8Q}   
pwn.college{fake_flag_number_16_imE2E7VwKBM}   
pwn.college{fake_flag_number_17_ADC3aneyvI8}   
pwn.college{fake_flag_number_18_IfuP9McmykI}   
pwn.college{fake_flag_number_19_IfcUBRtIDBI}  
pwn.college{fake_flag_number_20_n8vOLQC2GRU}   
pwn.college{fake_flag_number_21_7buHybJ18mw}   
pwn.college{fake_flag_number_22_4wFPZ4jM5g}  
pwn.college{fake_flag_number_23_vECu2CcIO3A}   
pwn.college{fake_flag_number_24_MmBxTHNl67M}   
pwn.college{fake_flag_number_25_A7xoi8oFnYA}   
pwn.college{fake_flag_number_26_rLBeNjAW2qE}   
pwn.college{fake_flag_number_27_z3Pmkuu10Tk}   
pwn.college{fake_flag_number_28_rc0iYxOlMC4}   
pwn.college{fake_flag_number_29_Rnuvs8UVtAw}   
pwn.college{fake_flag_number_30_68hkucr2So}   
pwn.college{fake_flag_number_31_rRO6JtIZiw}   
pwn.college{fake_flag_number_32_pW2w8KdrXk}   
pwn.college{fake_flag_number_33_1ncMF9QqzdU}   
pwn.college{fake_flag_number_34_9n1VmpzoyOc}  
pwn.college{fake_flag_number_35_owUtidHJqzA}   
pwn.college{fake_flag_number_36_x04E5PSaoas}  
pwn.college{fake_flag_number_37_sLSD8hLw9XM}   
pwn.college{fake_flag_number_38_UnSbX8YefmM}   
pwn.college{fake_flag_number_39_Zt2YZyT9U3M}   
pwn.college{fake_flag_number_40_tszrLnne0}   
pwn.college{fake_flag_number_41_TCmA1DYiuA0}   
pwn.college{fake_flag_number_42_5RTCevHZPuY}   
pwn.college{fake_flag_number_43_8a6Z2p646Mg}  
pwn.college{fake_flag_number_44_IdOSQCKHm70}   
pwn.college{fake_flag_number_45_0SabXjyNwI}   
pwn.college{fake_flag_number_46_1vcC6NnEifI}   
pwn.college{fake_flag_number_47_AgRIrya4Axs}   
pwn.college{fake_flag_number_48_bWfrjEDlmgY}   
pwn.college{fake_flag_number_49_n2PbjtEHerk}    
pwn.college{fake_flag_number_50_CnQe5bF3k}    
pwn.college{fake_flag_number_51_Wc6KDFl84}   
pwn.college{fake_flag_number_52_cWIZsgS488c}  
pwn.college{fake_flag_number_53_GoKPDILedo}  
pwn.college{fake_flag_number_54_as3ltngKkxM}  
pwn.college{fake_flag_number_55_DEQtdDIEC8w}  
pwn.college{fake_flag_number_56_fJFT3NHBuw}  
pwn.college{fake_flag_number_57_qApRH9149CY}  
pwn.college{fake_flag_number_58_b5iKsafXw4Y}  
pwn.college{fake_flag_number_59_MXlUV1lsm7E}  
pwn.college{fake_flag_number_60_khXtHkbd9gI}  
pwn.college{fake_flag_number_61_QaD2fhPxZw}  
pwn.college{fake_flag_number_62_TDvaXtAxJWg}  
pwn.college{U-1XWlQw1P-vIZ-Xjxu44mPm0kv.01MwMDOxwCO1gjNzEzW}  
pwn.college{fake_flag_number_63_4qvM6iw3MOQ}  
pwn.college{fake_flag_number_64_0K0wsy4wBIQ}  
pwn.college{fake_flag_number_65_MEeoPcokMI}  
pwn.college{fake_flag_number_66_tGzy6Zx0Jmo}  
pwn.college{fake_flag_number_67_9W7bBc6vi9w}  
pwn.college{fake_flag_number_68_cNNxeQlVyec}  
pwn.college{fake_flag_number_69_XUHmCkIR5g}  
pwn.college{fake_flag_number_70_EG8mPU5zj3o}  
pwn.college{fake_flag_number_71_UTNQFRhpvi8}  
pwn.college{fake_flag_number_72_JrYQTgKeDnU}  
pwn.college{fake_flag_number_73_9Y6VAXqAVs}  
pwn.college{fake_flag_number_74_8qTituVTWg}  
pwn.college{fake_flag_number_75_QGYxxHeNp5M}  
pwn.college{fake_flag_number_76_HQis4Dksppo}  
pwn.college{fake_flag_number_77_aGCRKJWG3zg}  
pwn.college{fake_flag_number_78_DvxXwEFgTaY}  
pwn.college{fake_flag_number_79_Kj3gjyThcRw}  
pwn.college{fake_flag_number_80_BRIc1UXHtIs}  
pwn.college{fake_flag_number_81_L3AQyR2VysM}  
pwn.college{fake_flag_number_82_XxnyBi5J6pA}  
pwn.college{fake_flag_number_83_jBBt1LaIyo}  
pwn.college{fake_flag_number_84_KUDX9WLllvM}  
pwn.college{fake_flag_number_85_9RxiEjOzTIQ}  
pwn.college{fake_flag_number_86_xVAt6K9ROz4}  
pwn.college{fake_flag_number_87_VwlzJFTSGlw}  
pwn.college{fake_flag_number_88_P4aKidRvUGM}  
pwn.college{fake_flag_number_89_Zy8ltGfenoM}  
pwn.college{fake_flag_number_90_6XohhjdfqM}  
pwn.college{fake_flag_number_91_2wDeGhK6Kg}  
pwn.college{fake_flag_number_92_9WtaaXY4ArU}   
pwn.college{fake_flag_number_93_wXr8jLljGA}    
pwn.college{fake_flag_number_94_zyYzPh2QauE}    
pwn.college{fake_flag_number_95_VF5XcAppnM}    
pwn.college{fake_flag_number_96_uBoebRRljpg}    
pwn.college{fake_flag_number_97_PUszhX3UbE}   
pwn.college{fake_flag_number_98_GLSkETo3gA}    
pwn.college{fake_flag_number_99_N3JPrDN00SY}   
pwn.college{fake_flag_number_100_qwEMyf499Y}  
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt    
62a63    
> pwn.college{U-1XWlQw1P-vIZ-Xjxu44mPm0kv.01MwMDOxwCO1gjNzEzW}    
hacker@commands~comparing-files:~$
'''

## What I learnt
I learnt that to compare 2 files which have a lot of data,instead of manually scanning them,we can use the 'diff' command which can be used to compare 2 files and mention instances wherein there's a difference between the 2 files.   

## References
None.    


<img width="654" height="874" alt="image" src="https://github.com/user-attachments/assets/b29143d0-8ddb-46a7-bf45-59190bedcda8" />     


<img width="654" height="889" alt="image" src="https://github.com/user-attachments/assets/a11dc2f1-c797-41b8-8b83-89b13311bc20" />      


<img width="654" height="889" alt="image" src="https://github.com/user-attachments/assets/aa7aa32d-4cfc-468b-86da-a352ea1a0bb9" />      



<img width="654" height="285" alt="image" src="https://github.com/user-attachments/assets/d9fabee5-4268-432c-8a1b-ab29031a60bb" />



