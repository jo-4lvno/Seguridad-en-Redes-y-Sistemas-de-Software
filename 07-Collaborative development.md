
**Descripción** 
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/179/challenge.zip)

**Solución** 
joaquina_alvno-picoctf@webshell:~/drop-in$ nano flag.py
joaquina_alvno-picoctf@webshell:~/drop-in$ git add flag.py
joaquina_alvno-picoctf@webshell:~/drop-in$ git commit
[main 1f4557f] Merge branch 'feature/part-2'
joaquina_alvno-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')
print("m@k3s_th3_dr3@m_", end='')
joaquina_alvno-picoctf@webshell:~/drop-in$ git merge feature/part-3
Auto-merging flag.py
CONFLICT (content): Merge conflict in flag.py
Automatic merge failed; fix conflicts and then commit the result.
joaquina_alvno-picoctf@webshell:~/drop-in$ nano flag.py
joaquina_alvno-picoctf@webshell:~/drop-in$ git add flag.py
joaquina_alvno-picoctf@webshell:~/drop-in$ git commit
[main 4f7b2a6] Merge branch 'feature/part-3'
joaquina_alvno-picoctf@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')
print("m@k3s_th3_dr3@m_", end='')
print("w0rk_798f9981}")