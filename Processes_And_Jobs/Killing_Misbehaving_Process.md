# Killing Misbehaving process
The challenge asks you to open the terminal in the pwn.college DOJO and invoke the 'kill' command to get the desired output.     

## My Solve 
**Flag:** 'pwn.college{w_8WewpGTZ4l6Tlc3pnEPNO_TIK.0FNzMDOxwCO1gjNzEzW}'

Here,we are asked to run '/challenge/run' to get the flag output which would be written into a pipe called '/tmp/flag_fifo'.But before that we need to kill the decoy which is hidden and can hinder the process.Hence we use the 'ps' command to find out the decoy and use the 'kill' command to kill the process.Then upon running '/challenge/run' it writes into the pipe '/tmp/flag_fifo'.But when we run the pipe,there's still a lot of decoys due to buffering of the shell.Hence by rerunning the previous 2 commands,we get the final flag output.    
'''      
Connected!                                                                            
hacker@processes~killing-misbehaving-processes:~$ ps -ef      
UID          PID    PPID  C STIME TTY          TIME CMD        
root           1       0  0 18:04 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h        
root           7       1  0 18:04 ?        00:00:00 /run/dojo/bin/sleep 6h      
root         137       1  0 18:04 ?        00:00:00 /bin/bash /challenge/.init      
root         138       1  0 18:04 ?        00:00:00 /bin/bash /challenge/.init       
root         139       1  0 18:04 ?        00:00:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker       
root         140     137  0 18:04 ?        00:00:00 sleep 6h      
root         141     138  0 18:04 ?        00:00:00 sleep 6h       
hacker       142     139  0 18:04 ?        00:00:00 /usr/bin/python /challenge/decoy          
hacker       144       0  0 18:04 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint       
hacker       150     144  0 18:04 pts/0    00:00:00 /run/dojo/bin/bash --login       
hacker       182       1  0 18:04 ?        00:00:00 /nix/store/nnkd8d66viqr8xg9vbiyhpjjgk2gzpf3-tigervnc-1.14.0/bin/Xvnc :0 -localhost 0 -rfbunixpath /run/dojo/var/desktop-service/Xvnc.sock -rfbauth /run/      
hacker       187       1  0 18:04 ?        00:00:00 /nix/store/ih68ar79msmj0496pgld4r3vqfr7bbin-bash-5.2p37/bin/bash /nix/store/41l19hq1cjclz00y09z77ilay6m814vs-novnc-1.6.0/bin/novnc --vnc --unix-target=/       
hacker       197     187  0 18:04 ?        00:00:00 /nix/store/h097imm3w6dpx10qynrd2sz9fks2wbq8-python3-3.12.11/bin/python3.12 /nix/store/vhjcb946r4swhvrfilwwhlainwd2izki-python3.12-websockify-0.13.0/bin/       
hacker       207       1  0 18:04 ?        00:00:00 /nix/store/81f2pmz7y9jz2xdh44wg4cycc6q8wlac-xfce4-session-4.20.2/bin/xfce4-session      
hacker       210       1  0 18:04 ?        00:00:00 /nix/store/zbydgvn9gypb3vg88mzydn88ky6cibaz-dbus-1.14.10/bin/dbus-launch --sh-syntax --exit-with-session --config-file=/nix/store/zbydgvn9gypb3vg88mzydn          
hacker       211       1  0 18:04 ?        00:00:00 /run/current-system/sw/bin/dbus-daemon --syslog --fork --print-pid 5 --print-address 7 --config-file /nix/store/zbydgvn9gypb3vg88mzydn88ky6cibaz-dbus-1.       
hacker       216       1  0 18:04 ?        00:00:00 /nix/store/97ycb61fb3vismhljpx5fwrgymxq2nwv-xfconf-4.20.0/lib/xfce4/xfconf/xfconfd      
hacker       225       1  0 18:04 ?        00:00:00 /run/dojo/bin/ssh-agent -s         
hacker       227     207  0 18:04 ?        00:00:00 xfwm4     
hacker       232     207  0 18:04 ?        00:00:00 xfsettingsd      
hacker       238       1  0 18:04 ?        00:00:00 /usr/libexec/dconf-service     
hacker       241     207  0 18:04 ?        00:00:00 xfce4-panel    
hacker       246     207  0 18:04 ?        00:00:00 Thunar --daemon    
hacker       253     207  1 18:04 ?        00:00:00 xfdesktop     
hacker       260     241  0 18:04 ?        00:00:00 /nix/store/wd6r31f7cx88p1gnmfkh7yij3nls87v4-xfce4-panel-4.20.4/lib/xfce4/panel/wrapper-2.0 /nix/store/wd6r31f7cx88p1gnmfkh7yij3nls87v4-xfce4-panel-4.20.     
hacker       357     197  1 18:05 ?        00:00:00 /nix/store/h097imm3w6dpx10qynrd2sz9fks2wbq8-python3-3.12.11/bin/python3.12 /nix/store/vhjcb946r4swhvrfilwwhlainwd2izki-python3.12-websockify-0.13.0/bin/     
hacker       360     150  0 18:05 pts/0    00:00:00 ps -ef     
hacker@processes~killing-misbehaving-processes:~$ kill 142      
hacker@processes~killing-misbehaving-processes:~$ /challenge/run      
Sending the flag to /tmp/flag_fifo!     
^C      
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo       
pwn.college{5C8kMt4fJIZhZXpA1d4O9c8Jm9XKIW2SohRMRqXTpHd4FRA}      
pwn.college{iVhVSXQ85XHngab.KNKBQVu9cy2gcDP5TInc0wVpa-tMEvV}     
pwn.college{-iGtX7YQDn9-szK58Shgkq90aoVSRD2G-dLyD8ITCJJqQTz}     
pwn.college{AhVgopYoTc8KLchQRA10Ghb6.HfK4BUjgS5tgzRGu.VktLC}     
pwn.college{x07h0mo2FxM.tvyQqNPUIiqUQcoJ5IfSSd-09rndjOYBkpR}     
pwn.college{KUZA7bqa8SEAbO56YE.tD6ooGg1dGTvansSqhMjZ2QroU6W}    
pwn.college{sM.sFUb1TiBiT4nPucOzBlGgdpcxYpLw2AUUNgo8VpHalKc}    
pwn.college{cI.WOb7XbR9w3nQnLetfqxV7IMh.7Cs6ymdoxci99gZ9LAr}     
pwn.college{8qaWloBzRq378Y-EVOvb61sm11mNNlFQ3AO3EKVTcwxxLNC}     
pwn.college{EE.k0oZPfN3xq4RR4L9aXDcaX.d0Hbg64snqrZDtsUpRuAo}     
pwn.college{CjbnGGb9ZJSVn1PBAf9dfTm3CgZqWFPHtD8rQWa0rayN.gP}     
pwn.college{u23AePi3jwk1bJD6NmJ1Oha3M6VqDg2dfnaLwocqUVTcx.d}     
pwn.college{sjNThB9dNp-OWJGf.vK1DQGfSNF02rPXFbw7.9ezCdXsmsi}      
pwn.college{2PiX80qrXGwV7FwV-J6Sllk4b6X6qp8rHmvMrTwONNEfZWu}     
pwn.college{tbTqvvAB1t.DlUpdxI9XWBuXOM8m4Wa2RKrfzMFjbp4cS9Z}      
pwn.college{yju-lddhvkLqM3bXX1frMBASfGMAxLnOWKt0XvmeyE1Rcw5}      
pwn.college{XOEyxw61tRr229osAEmWXFYspo.zJ4sfZBjW.1pokq4FWa4}    
pwn.college{stpmIv304oxU.XFXWJMuk1j0m7F8PwBuEw62W23o0Y01CDK}    
pwn.college{0FpSsk05bF9mYR8gd2QuoonFkwF31QJuuk3ibjFKmdCFroS}    
pwn.college{ylnrW6Pl5x33qeKsf.vMzy6h3lBcKjUsW3uGv7k9BGyycEr}    
pwn.college{raYYZHP-zXLAUHLge.kptJMxwzeO40XeNgDb8i1oofCdUEC}     
pwn.college{Ov3OsEwFp3gvuSlfNKP.lUgzz8.fiozMwU17EfniI.EgDn9}    
pwn.college{hvqzJ2rD3-nebGrM9L57UFx0X84nmaB66OyoF48191y1RjI}   
pwn.college{mjFmJZs1FhFKtdqfXBDuyllBxbxqHGSFsVfwF4A76Spdicu}    
pwn.college{uFjiIp0Si9nRv44AjECUQbYASO-gIuXhp5cbpQZOha1jQOA}   
pwn.college{-Dk-iL6FkrrtgYY7nLAEll2z58iw9.bRNwQ1ZLn5nqYzkvu}   
pwn.college{.JlfvKrKejG9uhnBwMjbPR7HJgl6EIvJVFKZgoIHOrs2Mrp}   
pwn.college{YmrvrKRzcHN5o2.Hd18cOqgR4N7XCzxx1GaOlYzT7Q9cT8i}   
pwn.college{-DJc8IF0QTlpTuj4fXKaTW4pnHrkRpy4ptk1hhO.Exwex04}   
pwn.college{8YyFa16ULAnZ1Dpr37yR77IgRRPwgzRe7zMWFl56lxdQza7}   
pwn.college{nBQwpOV7-3Ah4srQMkqRbKwg937B8hFLl5jCKXEnxY9EySx}   
pwn.college{eb.LZR5xKVdxJ28zhAOlMaESFd6XrWe5aoOgjUFucHdYizC}   
pwn.college{49Bm.NACrZubO2XtWz4XhyOocakCEXNCzmdj4QHtmu4tomY}   
pwn.college{IrPx-PRNGvjcQ58rG-marDo0SRSYEAX.YL3L8FLHF-m9jnj}   
pwn.college{uTjNCorTImTEZLlQZWUW0p8-rDV31rbzt1VE4E68YaN0..9}   
pwn.college{yQfnavUtO8.VG8U5hxNQALCZ9tGkYOUPr8aaRfQITm-Zjyu}   
pwn.college{xCuszspxdgee6vH4rQXex7xY-7B5.yjrLB.hDM4DjGdgbdm}    
pwn.college{H5ANlN5.rGPwIyXoTxfYIs3fqjJJbGvljYOManUNZIn8GME}    
pwn.college{VUYO.GTbbMCbu8Q2qmz0PPvTkGmlKRkKQdsqlSp286Amcdw}     
pwn.college{92EulpMWDkL5y-VmkMI6YGlFacqjQY1OjzNMe1QU8c.RnsL}   
pwn.college{dsBuis3IML8.BxsVhHsT6fCxDr2MEBMdlog3faH-Z9OpiMB}   
pwn.college{wfqX2vfmjGt3Ev7bhkWIcGJM6kRBpLkYsqbLOzxHqidmPx1}   
pwn.college{LO.RGgdqF7pbu0K.QeHDMaPq.sUmkmU5yRSGJ7teexCF1BY}   
pwn.college{ZVpndMxpvIiIuIPMFA9aIq6gsdC7O3PXG0lqcG74ZRDLUpC}   
pwn.college{k.mre2QGaUsLqNdYyIJefT0dfilnIrsnvP0nPS9k5-2..gR}   
pwn.college{jr2nHBG.tdzQjZD6y.7xMaXneWgTZpwqgw7t.NXbTOVZ.SG}    
pwn.college{YZhOy1c2mOvPF-4eMnNd.7EHA.PlLJpFzskqEDKNpHQnmvn}       
pwn.college{TJabQUciB34-SyOu4-oGjc2iUYxXmeCOuDk96VczUmTfX-Q}   
pwn.college{mzEya9VqnElYdogPhm0Ef0.gVhuh10jq22ir5ukKfPnrX01}   
pwn.college{kQUuxfCe4FL155wFfIkiKSfDUA97YgY.xd23.hHvNCCpEyX}   
pwn.college{EaRI3Znknls9fdbbGCHrhwGYFoQ-V-sQG4sOd-JdVj4latm}   
pwn.college{jCSUYD.V5C0eC3N8Hxz3hvHgzSC4ihrXQlSWJOTQb1.Rs8G}  
pwn.college{FMCsLW6xIp1pTcz3K0RrzIFzi98BuRBW6JjJYoGDwX5jonU}   
pwn.college{3yqW3xZYpP541MMMjTmWlLDLSKVqJiZ-BLKi0kllRwcTZt2}   
pwn.college{Mkk1iI-XWbK49w4-2Ew-P1s42E5rSuvLJgLnu82JZ7sby8v}   
pwn.college{sFAhEowTnsCW83ApL8vPik.mYB41TK9U5ePMoMKYYXkUcTz}   
pwn.college{G-rxRiceC0r99EPBjPGUBg1BwcIQlxHzDW-7YuC.UT5gT9t}   
pwn.college{Gdm11hzGrtSYtPsERz5kHZ8AfQEAufWIsieoowKOgdt9AxR}   
pwn.college{iM8al-ufA.xAiw5zTN8REJHVQ5.z7SBXRco7etey2IoXU1A}    
pwn.college{C9EwbihXJUkGYdYmRQf2zNkEF7yNCR7YG314b9A2HWhqTSN}     
pwn.college{P3.pwSt4zGVMV1hwzcEPBm.sVdVPw1vUDbITtcCpMyFF5hJ}   
pwn.college{MsrtS2DcoZm32eKV5g1xlMW.1kExQrMcoPOUU7S63Fbw6Ae}        
pwn.college{SEsJhKSifnwScxzS8Yif8G67D7wDWnTdLwo-p1f3SZwrAap}
pwn.college{BdF4oRCCfWwHPJI8lgbS5L.oJshCaUEjMVO4l7.MWUeB1Ml}     
pwn.college{1bwZzWoAFNUXajB1Iiqk1QaT4wxBKfdKmzNbs-vcXqGOdx1}
pwn.college{9AeCzdYYsTRYT4wGlP-wKdBEQ9xlr8xAFwRRojWn7BlD6ie}     
pwn.college{NpelOrgH9NSQVSy7LZQc1epHJYIQ0zQxEBh8GmVAWATlsb9}    
pwn.college{O0kvZNMkDFr6MOMPuBCI2dIRO.wHds5ZStdXFZ6iN5r-ZnK}    
pwn.college{YG.zuw-3O8Hhy-IvQFiyfENBg.c9E6HyY-NX.i.IqM8cGtK}    
pwn.college{LK3tJ7tWyoJTnW7aI5VAfEIGzv-gDH0Jmytr0V07DkyvYgD}    
pwn.college{bZQf768k5-KHY-cDQDTFUCN6d5zYuvOO2-w66N0zvZ.jW2Z}     
pwn.college{.zO9ik9rSDkAq.mh1Zm1YaoOyeJm7wAkIgD3WKJYpcA7lcC}       
pwn.college{IKGHJdjdPBkEix1711iJkvQjmCdA4c.U8DzaGVyi3iaXwp8}     
pwn.college{CHmlSE7tc56JE8CK7YM6kRMysVnWl-okLo2CB1rezH-r5dj}     
pwn.college{iePCUnoHn3uEKiOxOZw65mOp5BZ7J3sqId5p1El1Pr7ZNqx}    
pwn.college{Zm79ifJinNazuI-uhrTiWhh74iY3jBQqu.uMo8coOt2C1QO}    
pwn.college{2xXTEIQTdO-CI6gSjz2hFZ3wtsAGQ83z79knUiTtm5V.7DO}    
pwn.college{dtDvM5CFhmioHHuycrha3pn6GyMLo1LXJQK9eFmY-zM90S7}    
pwn.college{IVwlN7aOSJ0NS.-GITa0BRWZ3AdlXznCHHlqukltStfpIjg}     
pwn.college{CjrY7qRv9wAFJFE7IAUwzRCZp15s-mq43neWObE1U-BowY-}       
pwn.college{EnBEg3VQobg6VnLVFvhAKvjgom9X8tr-W-EisdP51VPXGfZ}     
pwn.college{g.doBQ6tf6vK3s3GmS4uGWf9gVNDxGPVdQZfZ5JphgjHsGT}     
pwn.college{TuOhqohW.CM5xf67Ilnnx.J3F1pU8LQ20qGPdyuCUapJl6n}    
pwn.college{5wV0OEUMnK3p-nKeQS6YkcGLx7dB0ISegIDo6QKx3Lj6Jje}    
pwn.college{OYarpb2V.aTT1iPRM18UoD2m-Dhr9wVmBQ8FcWOjlHjSm-9}    
pwn.college{8qNc1hbeOpUdLDdO-qCv550arEMUHACbqQh1HXGeuXMd3dP}    
pwn.college{bZpuuueJzAqEcZHic8O8dCG49ieWtqgLfPvaVK7B.Wf61He}     
pwn.college{04E4lPsCuY-eh-tNknk47yoVHL7epGAX4LmzljpxlLqOulr}      
pwn.college{1NuIQo56yh7.sCh5eEeKmzhLybWQoeXmBp9-KMjxbKIn8G7}     
pwn.college{QNTTXJa-8aFykj-yZEx5vy0uWLtoyJXSXO2nr-ON2DtGeBG}     
pwn.college{UTsobpFrew-AUZrIxhrznop68GZhJL-AuipDJjeQ.cPhGGe}    
pwn.college{2htyKH8yMF7ZDXFoCTydfik2Zwx2XRKNjKnxu-dQ2TYPQ98}    
pwn.college{QxQJ0CYpoOzM6z9lJ2K-ypCtcLXvMdlBMR168tTqZMrSIDL}    
pwn.college{5uolmFxyYZmZHYAFXmqfK56FenGO6mw7Qj2JZIMboQSNfmP}     
pwn.college{HCb6ScqFglnjeGmQkg7FrlAhXNY5PPzsqIAiUSV0bMjPvrg}     
pwn.college{SSXaY.3T1DwQ7aSVN-8v1keGiT1QC0AviiLIWultEe7.zit}     
pwn.college{w3yNAvB0A0fxZunH7-OTX9sdsUwZ5C5LYAavkcC1L52dIun}     
pwn.college{Iw7yQCXZD8.CmGf3jLdaRwDgURye3XJR-fpVFnKtdn0--SM}     
pwn.college{gl6BIv5Am5Ez8HAAUGDErpfurOjVAp9JIe7n28Y1TeW7XsK}     
pwn.college{nLLmwlpWiq3w9cBE.X8IFcSjT.yqS8hudv1chWb1aY211PL}    
pwn.college{c59PfUkczqf3L9PtlyHl54mm.7.yhy23HUCta3LVtUxLNv5}    
pwn.college{IjCBT85CF1W4nFFto1COa1WxsA1xxXwsbxSoVmQgblRe9bp}     
pwn.college{aYxywj7jSCR2jRhGqZWTvi7PYzVYksGCKJh8bft8e8saYly}    
pwn.college{SHFURW4G0lmYotll.zn2a5kQXynxHMCERCzGG8oGwyDc0zn}    
pwn.college{eg3xvbNT6DG0o6zfwuaDnWFhEDvyF-tElW6siAU.C.pgED6}     
pwn.college{nMHc2NyIM05PZBGlB1YO5-dWLUYTOQci.9BjHhkodvu8odE}     
pwn.college{i2ypRJ2JwNXdsmpREg4OiBsNxvtEDYa-gBxIQtRJS-eQ4At}      
pwn.college{lb87bJmcM2HgwYAZcWJtWRWFSzwKqetBWsnMxHlrvvZq7dX}     
pwn.college{Km149N2Jyaohhz4Unqd5y0Wq.mzsImrv5JNcgy46H4LAIL.}    
pwn.college{5IRNeoE09wTAKQU0DCx6fApKNll9wuRDavMnDyLP.deym-5}    
pwn.college{lANs4K2-Tl2NNwlBsOdzK5XfUdGyINnxbKJ4j2a9IEECGyv}     
pwn.college{xXDjgSM2h-v8eZ9UJp09gz0vZAYHGyq3hFHKnv4j4SUAg6q}    
pwn.college{vGYOdrkpGWvsjJlmEw9BpQyO4x-RSC-Q.wE0FIN6o6wNXmc}    
pwn.college{CUg.pXZ.ez4CvRAdph8O0iWbjXeonSUz78WyB1q05ZzghP8}    
pwn.college{d4bXlrfcS4lsDhodYs4PCC9lYsV-.S4eekrUnSpqVOQnG4L}     
pwn.college{nYRFvsVkg4vtAbsM7ojYVapf1tbEKF9jMBk1WomVayHuIZh}      
pwn.college{.LPU-V7exV8TrpA3UZrhzxkk5-xOpkLupwibDZZ3tUV5hAi}      
pwn.college{eeWz32DvgkYxYPM2Fsed2MwY7CMPM9txoJRuvsjga8c4qGu}     
pwn.college{Nor7ZYEZfSvFsJfTSZdtbdpaWz4WFDXewHUBY97f2lf-I2B}     
pwn.college{JPP4sNU-hjSh1Yn8fyW8CLS9FHf960rebO0IrDGoMKkKZIF}     
pwn.college{y8x0Mr0PCpzyH.jNRF7LQfad9oQjAjC.yZi9o5tuapmpUJ-}      
pwn.college{99ecrg0XS5iiGObAHJ.0j5rhY-XZaa0S2LVVflw1CTGCzAi}       
pwn.college{gS1.mrkATwZo4XwB1V8GDpWZq7gjdaKz6xj0XrDVwIehbin}       
pwn.college{aQJDTMeptPxazmOKzyEJhU2b5UDiIHl3kvNOrpD0DCUA3nh}      
pwn.college{RlRsCqVn2ksRSKV.62LMJYDxz.F-HPXmJjhyNiDEygOhdiA}      
pwn.college{cduFCMN2xh-qQExWYhT069i5iqRp.dHfmGv7gwF1nzIK6Xs}     
pwn.college{AFDae.WtO7fqE8R0CO-cqJYqz5A1ggt.pqqZxkm79DrCm-v}     
pwn.college{lVNV76HLH-VaYnE2styghaVZ8t9UAsngLhzzbzqjHV.00WX}     
pwn.college{FAFnf5TgOoRXcnFqZYWk2JfFJn8pmw8h-1GCl20NMeYT.G-}      
pwn.college{ay8BpuWGmHFkJiWKwpI34yewHrgXlby8g-3tNzPUFnruX5X}      
pwn.college{JXKHb8uWZnaoAUc4ubCjeFsm3ST3ay1iw.M4.skWyMbigv6}       
pwn.college{qtNd0QlDDByw4CyVBIcWusUXYnVms8VKyjuDkoHNUDz.eTU}       
pwn.college{xLwsEktzZa-S.sKqScS6JL6YZiX19W.94WLoNNi0H7XLLjy}     
pwn.college{y8OeBqMPlK3.KBStXR9XSqmtKKmxB5zx.NwqC2WKVD7qhpx}       
^C     
hacker@processes~killing-misbehaving-processes:~$ /challenge/run     
Sending the flag to /tmp/flag_fifo!        
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo          
pwn.college{w_8WewpGTZ4l6Tlc3pnEPNO_TIK.0FNzMDOxwCO1gjNzEzW}       
^C       
hacker@processes~killing-misbehaving-processes:~$         
'''      

## What I Learnt 
I learnt the usage of the 'kill' command to kill a decoy process and the usage of pipes to connect 2 commands.    

## References
None.     

<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/13161070-62da-4d91-b84b-6bdfaf2f582d" />      


<img width="1440" height="730" alt="image" src="https://github.com/user-attachments/assets/06e116ec-4401-474b-a062-0230d700bb6e" />       


<img width="1440" height="900" alt="image" src="https://github.com/user-attachments/assets/58742b50-7cb7-48c9-81c5-1d65890ad144" />        
