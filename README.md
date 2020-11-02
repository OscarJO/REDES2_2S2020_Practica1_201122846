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

PROCESO PARA PROYECTO 2

14. Se crea una segunda instancia idéntica a la primera en donde también se instale el servidor apache y se reemplace al página default.
15. Creamos un load ballancer.
16. En el apartado 'Equilibrio de Carga' seleccionamos la opción 'Crear Load Balancer' y elegimos el balanceador clásico.
17. Le asignamos un nombre al balanceador.
18. Dejamos el protocolo por default que el HTTP en el puerto 80.
19. Asignamos el grupo de seguridad correcto.
20. Se seleccionan las instancias que van a utilizar el balanceador.
21. Se agregan tags para el balanceador.
22. Se termina de crear el balanceador y esperamos a que todo se inicie.
23. Cuando todo está funcionando, utilizamos la dirección de DNS que nos proporciona el balanceador y esa será la dirección que utilizamos.
24. Lo siguiente es hacer las configuraciones del Route 53 para poder redireccionar el balanceador hacia el nombre de dominio creado anteriormente.
24. Nos dirigimos al apartado con el servicio 'Route 53'.
25. En las opciones elegimos 'Crear zona alojada'.
26. Llenamos el nombre de dominio con el dominio que creamos.
27. Dejamos la opción 'Zona alojada pública' seleccionada.
28. Termina al proceso de crear la zona y se nos redirecciona a la zona creada.
29. Nos dirigimos al sistio web en donde se creo el dominio (en este caso en my.freenom.com) y entramos a la configuración del dominio.
30. Elegimos la opción de administrar el dominio y entramos a la opción de 'Nameserver'.
31. Copiamos los nameservers que la zona alojada nos proporciona y los pegamos en el sitio del dominio como nuevos nameservers.
32. En la consola de administración de la zona alojada elegimos la opción 'Crear registro'.
33. Seleccionamos la opción 'Registro simple'. 
34. Nos presenta una ventana donde nos pide ciertos datos (el prefijo para el dominio, la locación del servidor, etc.).
35. Es importante que se elija la opción 'Alias del Classic Load Balancer' para que nos deje elegir el balanceador que creamos como opción de redireccionamiento.
36. Elegimos la opción 'Definir registro simple'.
37. Esperamos que se inicien los servicios y luego ya podremos acceder a las páginas definidas en el balanceador por medio de nuestro nombre de dominio.