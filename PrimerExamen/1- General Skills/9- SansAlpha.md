# Reto
# Descripcion
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.

Additional details will be available after launching your challenge instance.
# Solucion

```
joaquina_alvno-picoctf@webshell:~$ ssh -p 55096 ctf-player@mimas.picoctf.net
The authenticity of host '[mimas.picoctf.net]:65497 ([52.15.88.75]:65497)' can't be established.
ED25519 key fingerprint is: SHA256:n/hDgUtuTTF85Id7k2fxmHvb6rrLrACHNM6xLZ46AqQ
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[mimas.picoctf.net]:65497' (ED25519) to the list of known hosts.
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@mimas.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

SansAlpha$ ls
SansAlpha: Unknown character detected
SansAlpha$ ./*
bash: ./blargh: Is a directory

SansAlpha$ ./*/*
bash: ./blargh/flag.txt: Permission denied

SansAlpha$ /?
bash: /?: No such file or directory

SansAlpha$ /???
bash: /bin: Is a directory

SansAlpha$ /????
bash: /boot: Is a directory

SansAlpha$ /???????
bash: /???????: No such file or directory

SansAlpha$ /???/??????
/bin/base32: extra operand ‘/bin/base64’
Try '/bin/base32 --help' for more information.

SansAlpha$ /???/????64 /????/??????????/??????/????????
/bin/base64: extra operand ‘/bin/x86_64’
Try '/bin/base64 --help' for more information.

SansAlpha$ /???/???[1_]64 /????/??????????/??????/????????
x86_64: failed to execute /home/ctf-player/blargh/flag.txt: Permission denied

SansAlpha$ /???/???[!_]64 /????/??????????/??????/????????
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV9iMGQ1ZTg1NX0=

SansAlpha$  

```

[decodificado](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y21WMGRYSnVJREFnY0dsamIwTlVSbnMzYURFMVgyMTFNVGN4ZGpOeU5UTmZNVFZmYlRSa2JqTTFOVjgyTkRCaU5tRmtaSDA9)
### Flag: picoCTF{7h15_mu171v3r53_15_m4dn355_b0d5e855}
# Notas
Al ingresar al servidor me di cuenta que no importa que escriba es invalido, para evitar eso utilcie uina tecnica de globbing y wildcards donde los simnolos ? y * son como comodines para los caracteres desconocidos. Tras explorar el directorio actual con ./* intente abrir directamente el archivo flag pero no tenia permisos de lectura, se me ocurrio ejecutar archivos binarios que lo encontraba como /???.
El objetivo fue invocar /bin/base64 para leer el archivo y codificarlo, evadiendo la restricción. Para diferenciar entre base32 y base64 sin usar letras, se aplicó una expresión regular de corchetes [!_ ] 64 para excluir caracteres no deseados y seleccionar el binario correcto. Finalmente, la cadena en Base64 resultante se decodificó localmente para obtener la bandera.
