
**Descripción** 
How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 62224
Username: picoplayer 
Password: kZx-HVJKu8
```


**Solución**

joaquina_alvno-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 62224
The authenticity of host '[saturn.picoctf.net]:62224 ([13.59.203.175]:62224)' can't be established.
ED25519 key fingerprint is SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:62224' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
picoplayer@challenge:~$ cat /etc/crontab
picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
