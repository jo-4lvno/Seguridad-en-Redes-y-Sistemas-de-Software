
**Descripción** 
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

**Solución**
joaquina_alvno-picoctf@webshell:~$ ls -la level3.hash.bin
-rw-rw-r-- 1 joaquina_alvno-picoctf joaquina_alvno-picoctf 16 Mar 16  2023 level3.hash.bin
joaquina_alvno-picoctf@webshell:~$ wc -c level3.hash.bin
16 level3.hash.bin
joaquina_alvno-picoctf@webshell:~$ hexdump -C level3.hash.bin | sed -n '1,6p'
00000000  16 02 6d 60 ff 9b 54 41  0b 34 35 b4 03 af d2 26  |..m`..TA.45....&|
00000010
joaquina_alvno-picoctf@webshell:~$ cat > find_level3_pw.py <<'PY'
> import hashlib
> from pathlib import Path
> 
> candidates = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]
> hbin = Path('level3.hash.bin').read_bytes()
> 
> for pw in candidates:
>     if hashlib.md5(pw.encode()).digest() == hbin:
>         print("FOUND", pw)
>         break
> else:
>     print("No match found")
> PY
joaquina_alvno-picoctf@webshell:~$ 
joaquina_alvno-picoctf@webshell:~$ python3 find_level3_pw.py
FOUND 2295
joaquina_alvno-picoctf@webshell:~$ printf "2295\n" | python3 level3.py
Please enter correct password for flag: Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
