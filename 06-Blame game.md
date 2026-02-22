
**Descripción** 
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/74/challenge.zip)

**Solución**  
despues de descomprimir
joaquina_alvno-picoctf@webshell:~$ cd drop-in
joaquina_alvno-picoctf@webshell:~/drop-in$ git status
On branch master
nothing to commit, working tree clean
joaquina_alvno-picoctf@webshell:~/drop-in$ git log
joaquina_alvno-picoctf@webshell:~/drop-in$ cd drop-in
-bash: cd: drop-in: No such file or directory
joaquina_alvno-picoctf@webshell:~/drop-in$ ls       
message.py
joaquina_alvno-picoctf@webshell:~/drop-in$ git blame message.py
picoCTF{@sk_th3_1nt3rn_ea346835}