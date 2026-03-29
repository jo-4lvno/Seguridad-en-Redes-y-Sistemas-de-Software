
**Descripción** 
ROJO, ROJO, ROJO, ROJODescarga la imagen: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)

**Solución**  
- Descargar el archivo
- Hacer un `exiftool red.png`
- En los metadatos sale un Poema
- Ese poema contiene mayusculas que si las unes dice "CHECK LSB"
- Hacemos un :`zsteg red.png`
- En el lsb hay un archivo codificado en base 64
- Lo decodificamos y la bandera es: **picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}** 
