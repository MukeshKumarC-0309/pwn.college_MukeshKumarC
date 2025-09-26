# An Epic Filesystem Quest
The challenge asks you to open the terminal in the pwn.college DOJO and we had to follow a step of commands to get the desired output.  

## My Solve
**Flag:** 'pwn.college{44tX88ib-gjhFDyTwH9oj4MPbu2.QX5IDO0wCO1gjNzEzW}'     

First,the clue is hidden in the '/' directory.Hence we use the ls command to see all the files.Among them is the first clue,a file named 'BRIEF',which upon opening shows us our second clue,which says the location of our next clue(ie./usr/share/racket/pkgs/scheme-lib/scheme/unsafe/compiled) and says that it’s readable ie.can't be read until we change into that directory.Hence we use the 'cd' command to switch to said directory.Then upon using 'ls' command again,we find the next clue,'README' file which upon opening shows us the next location but this time it’s trapped ie.we have to access it without switching directories.Hence we use the 'ls' command with the absolute file path to see its contents.We find the next clue,"BLUEPRINT-TRAPPED" file which we open using the cat function with the absolute file path as its arguement,which also shows us the clue ie.location where we must go next which is delayed impyling we must switch to the directory to make it readable.We do that using the 'cd' command and then we use the 'ls' command to view its contents.Among them is the next file 'MESSAGE' which we open using the 'cat' command.Inside the file is the next location,which we change to using the 'cd' command.Then when we look through its contents using the 'ls' command,we find a file named 'INFO' which holds the next location,where the file is hidden.Hence this time we use the 'ls' command with the '-a' prompt to view the hidden files,among which there's '.LEAD' our next clue.We open it using the 'cat' command and the absolute file path as its arguement,which again leads us to our next location wherein the file is hidden again.We use the 'ls' command with the '-a' prompt again for the new directory(location).We find the next clue,a file named '.TEASER'.On opening it with the 'cat' command we get oru next location wherein again the file is hidden.Again we use the 'ls' command with the '-a' prompt to locate the hidden file,in this case the '.EVIDENCE' file,which on opening shows the location of the next clue.We use the 'cd' command to switch the directory.On using the 'ls' command,we find the list of files in it among which is the file 'MEMO' which on opening gives us the desired output(ie.flag).   
'''    
hacker@commands~an-epic-filesystem-quest:~$ ls /     
BRIEF  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var     
hacker@commands~an-epic-filesystem-quest:~$ cat /BRIEF      
Great sleuthing!      
The next clue is in: /usr/share/racket/pkgs/scheme-lib/scheme/unsafe/compiled      
      
The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.      
hacker@commands~an-epic-filesystem-quest:~$ cd /usr/share/racket/pkgs/scheme-lib/scheme/unsafe/compiled      
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scheme-lib/scheme/unsafe/compiled$ ls       
README  ops_rkt.dep  ops_rkt.zo      
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scheme-lib/scheme/unsafe/compiled$ cat README        
Congratulations, you found the clue!       
The next clue is in: /usr/lib/python3/dist-packages/sympy/matrices/expressions/tests/__pycache__       
        
Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!        
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scheme-lib/scheme/unsafe/compiled$ ls /usr/lib/python3/dist-packages/sympy/matrices/expressions/tests/__pycache__     
BLUEPRINT-TRAPPED              test_blockmatrix.cpython-38.pyc  test_dotproduct.cpython-38.pyc      test_hadamard.cpython-38.pyc   test_matadd.cpython-38.pyc   test_slice.cpython-38.pyc     
__init__.cpython-38.pyc        test_derivatives.cpython-38.pyc  test_factorizations.cpython-38.pyc  test_indexing.cpython-38.pyc   test_matexpr.cpython-38.pyc  test_trace.cpython-38.pyc    
test_adjoint.cpython-38.pyc    test_determinant.cpython-38.pyc  test_fourier.cpython-38.pyc         test_inverse.cpython-38.pyc    test_matmul.cpython-38.pyc   test_transpose.cpython-38.pyc      
test_applyfunc.cpython-38.pyc  test_diagonal.cpython-38.pyc     test_funcmatrix.cpython-38.pyc      test_kronecker.cpython-38.pyc  test_matpow.cpython-38.pyc      
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scheme-lib/scheme/unsafe/compiled$ cat /usr/lib/python3/dist-packages/sympy/matrices/expressions/tests/__pycache__/BLUEPRINT-TRAPPED     
Lucky listing!       
The next clue is in: /opt/linux/linux-5.4/drivers/net/ethernet/freescale       
         
The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.      
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scheme-lib/scheme/unsafe/compiled$ cd /opt/linux/linux-5.4/drivers/net/ethernet/freescale      
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/net/ethernet/freescale$ ls      
Kconfig  Makefile  dpaa2  fec.h       fec_mpc52xx.c  fec_mpc52xx_phy.c  fman     fsl_pq_mdio.c  gianfar.h          ucc_geth.c  ucc_geth_ethtool.c      
MESSAGE  dpaa      enetc  fec_main.c  fec_mpc52xx.h  fec_ptp.c          fs_enet  gianfar.c      gianfar_ethtool.c  ucc_geth.h  xgmac_mdio.c      
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/net/ethernet/freescale$ cat MESSAGE         
Congratulations, you found the clue!       
The next clue is in: /usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi      
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/net/ethernet/freescale$ cd /usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi      
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi$ ls       
INFO  __init__.py  __pycache__  cdp.py  console.py  script.py  session.py      
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi$ cat INFO     
Yahaha, you found me!       
The next clue is in: /opt/linux/linux-5.4/drivers/pinctrl/zte     
       
The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.     
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi$ ls -a /opt/linux/linux-5.4/drivers/pinctrl/zte      
.  ..  .LEAD  Kconfig  Makefile  pinctrl-zx.c  pinctrl-zx.h  pinctrl-zx296718.c      
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi$ cat /opt/linux/linux-5.4/drivers/pinctrl/zte/.LEAD      
Lucky listing!    
The next clue is in: /usr/local/lib/python3.8/dist-packages/numpy/distutils/checks      
      
The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.       
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi$ ls -a /usr/local/lib/python3.8/dist-packages/numpy/distutils/checks      
.            cpu_asimddp.c   cpu_avx2.c        cpu_avx512_knl.c  cpu_avx512f.c  cpu_neon.c        cpu_sse.c    cpu_sse42.c  cpu_vsx3.c  cpu_vxe2.c             extra_avx512f_reduce.c     
..           cpu_asimdfhm.c  cpu_avx512_clx.c  cpu_avx512_knm.c  cpu_f16c.c     cpu_neon_fp16.c   cpu_sse2.c   cpu_ssse3.c  cpu_vsx4.c  cpu_xop.c              extra_vsx4_mma.c      
.TEASER      cpu_asimdhp.c   cpu_avx512_cnl.c  cpu_avx512_skx.c  cpu_fma3.c     cpu_neon_vfpv4.c  cpu_sse3.c   cpu_vsx.c    cpu_vx.c    extra_avx512bw_mask.c  extra_vsx_asm.c     
cpu_asimd.c  cpu_avx.c       cpu_avx512_icl.c  cpu_avx512cd.c    cpu_fma4.c     cpu_popcnt.c      cpu_sse41.c  cpu_vsx2.c   cpu_vxe.c   extra_avx512dq_mask.c  test_flags.c      
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi$ cat /usr/local/lib/python3.8/dist-packages/numpy/distutils/checks/.TEASER       
Yahaha, you found me!       
The next clue is in: /opt/linux/linux-5.4/include/soc/fsl/qe          
          
The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.          
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi$ ls -a /opt/linux/linux-5.4/include/soc/fsl/qe       
.  ..  .EVIDENCE  immap_qe.h  qe.h  qe_ic.h  qe_tdm.h  ucc.h  ucc_fast.h  ucc_slow.h        
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi$ cat /opt/linux/linux-5.4/include/soc/fsl/qe/.EVIDENCE       
Yahaha, you found me!       
The next clue is in: /usr/share/mysql/korean      
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/selenium/webdriver/common/bidi$ cd /usr/share/mysql/korean      
hacker@commands~an-epic-filesystem-quest:/usr/share/mysql/korean$ ls      
MEMO  errmsg.sys       
hacker@commands~an-epic-filesystem-quest:/usr/share/mysql/korean$ cat MEMO       
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!       
It is: pwn.college{44tX88ib-gjhFDyTwH9oj4MPbu2.QX5IDO0wCO1gjNzEzW}       
hacker@commands~an-epic-filesystem-quest:/usr/share/mysql/korean$         
'''   

## What I Learnt
I learnt the combined use of all commands in order to traverse through different directories to find our desired file.      

## References
None.


<img width="1440" height="589" alt="image" src="https://github.com/user-attachments/assets/c5eace7e-14fb-4568-ad2b-95bdb338d233" />     


<img width="1440" height="396" alt="image" src="https://github.com/user-attachments/assets/c20da73b-8ecb-42f8-b509-01a6c378dd6f" />




