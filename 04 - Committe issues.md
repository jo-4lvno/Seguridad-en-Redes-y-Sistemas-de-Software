
**Descripción** 
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/137/challenge.zip)

**Solución**
descomprimir zip

joaquina_alvno-picoctf@webshell:~$ cd drop-in
joaquina_alvno-picoctf@webshell:~/drop-in$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        message.py

nothing added to commit but untracked files present (use "git add" to track)
joaquina_alvno-picoctf@webshell:~/drop-in$ git log
joaquina_alvno-picoctf@webshell:~/drop-in$ ls -a
.  ..  .git  message.py  message.txt
joaquina_alvno-picoctf@webshell:~/drop-in$ git log
joaquina_alvno-picoctf@webshell:~/drop-in$ git checkout ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0
Note: switching to 'ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ea859bf create flag
joaquina_alvno-picoctf@webshell:~/drop-in$ ls
message.py  message.txt
joaquina_alvno-picoctf@webshell:~/drop-in$ cat message.txt
picoCTF{s@n1t1z3_cf09a485}