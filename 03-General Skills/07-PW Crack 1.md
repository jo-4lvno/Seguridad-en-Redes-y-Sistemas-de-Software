
**Descripción** 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.

**Solución**
- Descargar ambos archivos
joaquina_alvno-picoctf@webshell:~$ printf "691d\n" | python3 level1.py
Please enter correct password for flag: Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_56891419}
