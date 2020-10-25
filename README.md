REDES2_2S2020_Practica1_201122846

PROCESO PARA PRACTICA 1

1. Crear una instancia EC2.
2. En la parte de configurar grupos de seguridad, dejamos por el momento la regla SSH y agregamos una HTTP de entrada en el puerto 80.
3. Iniciar la instancia creada.
4. Conectarse a la instancia por medio de la consola de AWS o cualquier herramienta de SSH.
5. Instalar apache en la instancia.
6. Utilizamos el comando 'sudo systemctl status apache'.
7. Luego de ese comando, se mostrará en la pantalla si el servidor se ha iniciado de manera correcta.
8. De estar correctamente iniciado, vamos al navegador y se ingresa a la dirección 'IP-Instacia:80'.
9. Se debería mostrar la página por default de apache.
10. Creamos una página HTML para reemplazar el default de apache.
11. Se reemplaza el archivo 'index.html' en el directorio default de apache (usualmente suele ser '/var/www/html') por el archivo html que acabamos de crear.
12. Al ingresar a la dirección 'IP-Instacia:80' ahora debería mostrar la página con la que reemplazamos a la página default.
13. Si todavía aparece la página default podemos reiniciar el navegador o borrar el caché de la página y luego ya debe aparecer el sitio ya reemplazado.