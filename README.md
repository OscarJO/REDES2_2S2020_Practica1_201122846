REDES2_2S2020_Practica1_201122846

PROCESO PARA PRACTICA 1

1. Crear una instancia EC2.
2. Configurar apache server en la instancia.
3. Iniciar los servicios con el comando '$ sudo service httpd start'.
4. Crear un punto de montaje.
	4.1. Crear un directorio 'efs-mount-point under /var/www/html'.
	4.2. Montar el sistema de archivos con el comando 'sudo mount -t efs fs-12345678:/ /var/www/html/efs-mount-point'.
5. Añadir la regla para el grupo de seguridad.
	5.1. Abrir la consola de la instancia.
	5.2. Elegir la opción 'Grupos de seguridad'.
	5.3. Elegir la opción 'Crear grupo de seguridad'.
	5.4. Poner un nombre al grupo de seguridad.
	5.5. Seleccionar el nombre de la VPC.
	5.6. Crear el grupo.
	5.7. En la consola, verificar las reglas por defecto del grupo recién creado.
	5.8. Agregar una nueva regla eligiendo el protocolo HTTP.
	5.10. Asegurarse que la regla sea válida para conexiones entrantes y salientes.
6. 