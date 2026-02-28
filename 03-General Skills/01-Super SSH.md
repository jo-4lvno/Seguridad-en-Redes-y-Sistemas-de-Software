
**Descripción** 
Using a Secure Shell (SSH) is going to be pretty important.

Additional details will be available after launching your challenge instance.

**Solución**
joaquina_alvno-picoctf@webshell:~$ ssh ctf-player@titan.picoctf.net -p65512   
The authenticity of host '[titan.picoctf.net]:65512 ([3.139.174.234]:65512)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:17: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:65512' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_3e293eea}
Connection to titan.picoctf.net closed.



