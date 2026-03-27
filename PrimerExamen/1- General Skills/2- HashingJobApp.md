# Reto
# Descripcion
If you want to hash with the best, beat this test!

Additional details will be available after launching your challenge instance.
# Solucion

```
joaquina_alvno-picoctf@webshell:~$ nc saturn.picoctf.net 53204
Please md5 hash the text between quotes, excluding the quotes: 'Abraham Lincoln'
Answer: 
9lease md5 hash the text between quotes, excluding the quotes: 'Abraham Lincoln'
Answer: 9lease md5 hash the text between quotes, excluding the quotes: 'Abraham Lincoln'
Incorrect. Try again?
Answer: 
lease md5 hash the text between quotes, excluding the quotes: 'Abraham Lincoln'
Answer: Answer: lease md5 hash the text between quotes, excluding the quotes: 'Abraham Lincoln'
Incorrect. Goodbye. Better luck next time!

joaquina_alvno-picoctf@webshell:~$ nc saturn.picoctf.net 53204
Please md5 hash the text between quotes, excluding the quotes: 'bull fight'
Answer: 
87cc16b261803de4f24debfd23119443
87cc16b261803de4f24debfd23119443
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'carnival workers'
Answer: 
d3818fc79b44a9f961c502fb3a9bd42d
d3818fc79b44a9f961c502fb3a9bd42d
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'assembly lines'
Answer: 
f8ad2642937fc973fb27821a6c047e7e
f8ad2642937fc973fb27821a6c047e7e
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}
```
[md5 hash generator](https://www.md5hashgenerator.com/)
### Flag: picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}
# Notas
El programa requiere calcular el hash de palabras, utilice una herramienta para que lo calcule y me de el resultado en hexadecimal. Ingrese correctamente los hashes y me dio la bandera.
# Referencias
