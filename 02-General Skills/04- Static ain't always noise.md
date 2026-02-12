**Descripcion**

Can you look at the data in this binary? The bash script might help![static](https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/static), [ltdis.sh](https://challenge-files.picoctf.net/c_wily_courier/b6c2dd492eb053dfbb3fcfa9eb142c8d11f6a00c0691031fc92b045d65b6e56a/ltdis.sh)


**Solución**
joaquina_alvno-picoctf@webshell:~$ ./ltdis.sh
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
joaquina_alvno-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
joaquina_alvno-picoctf@webshell:~$ ls
README.txt  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt
joaquina_alvno-picoctf@webshell:~$ cat static.ltdis.strings.txt | grep pico 
   3020 picoCTF{d15a5m_t34s3r_20335e41}

**Referencias**