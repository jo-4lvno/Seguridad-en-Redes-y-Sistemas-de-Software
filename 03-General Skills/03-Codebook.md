
**Descripción** 
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)

**Solución**

joaquina_alvno-picoctf@webshell:~$ sed -n '1,200p' code.py
joaquina_alvno-picoctf@webshell:~$ sed -n '1,200p' codebook.txt
azbycxdwevfugthsirjqkplomn
joaquina_alvno-picoctf@webshell:~$ python3 code.py codebook.txt
picoCTF{c0d3b00k_455157_7d102d7a}
