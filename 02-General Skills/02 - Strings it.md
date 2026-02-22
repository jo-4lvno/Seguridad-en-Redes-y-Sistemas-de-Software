**Descripcion** 
Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/6577d3f1500aebcd300787bd5d96216b30aed379c811f5e83e888f897da4a3d5/strings) without running it?

**Solucion**
joaquina_alvno-picoctf@webshell:~$ chmod +x strings
joaquina_alvno-picoctf@webshell:~$ ./strings
Maybe try the 'strings' function? Take a look at the man page
joaquina_alvno-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_d6306c19}