
**Descripción** 
Cada archivo recibe una bandera.El analista del SOC vio que una imagen se enviaba de un lado a otro entre dos personas. Decidieron investigar y descubrieron que había algo más de lo que parecía a simple [vista](https://artifacts.picoctf.net/c/261/flag.png) .

**Solución**  
- Descargar la imagen
- Revisar la estructura del png: ``pngcheck -v flag.png
- Descomprimir el archivo: `unzip flag.png`
- Abrir la imagen y esta es la bandera:
		**picoCTF{Hiddinng_An_imag3_within_@n_ima9e_96539bea}**


