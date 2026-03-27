
# Descripción
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.The website is running [picoCTF News](http://verbal-sleep.picoctf.net:54840/).
# Solucion

```
joaquina_alvno-picoctf@webshell:~$ wget http://verbal-sleep.picoctf.net:51368/heapdump -O heapdump
joaquina_alvno-picoctf@webshell:~$ file heapdump 
heapdump: ASCII text, with very long lines (64680)
joaquina_alvno-picoctf@webshell:~$ strings heapdump | grep picoCTF
picoCTF{Pat!3nt_15_Th3_K3y_59106086}
```
### Flag: picoCTF{Pat!3nt_15_Th3_K3y_59106086}

# Notas
Dentro de la pagina habia un href que te llevaba a la api de la pagina, homo se llama head-dump el reto descarge el heapdump de la pagina, al ver que era un ascii extenso lo imprimi con grep pico y me dio la bandera
