## APLICACIÓN WEB INFORMACIÓN METEOROLÓGICA ##

## Manual ##

1. Nos situamos en una consola en el directorio de la aplicación y ejecutamos (Docker debe estar iniciado):
docker-compose up -d

2. Abrimos un navegador, buscamos localhost:8088 y nos identificamos con usuario root y contraseña 1234

3. Comprobamos que está la base de datos euskalmet

4. Volvemos a la consola, ejecutamos en el mismo directorio que antes:
docker-compose up myapi bash

5. Una vez dentro del servicio, ejecutamos:
php artisan migrate

6. Comprobamos que se han creado las tablas en phpMyAdmin

7. Ejecutamos:
php artisan schedule:work

8. Comprobamos que se actualizan los datos volviendo al navegador en phpMyAdmin. En la tabla markers, la fecha de la columna dt tiene que ser similar a la actual

9. Accedemos a la aplicación frontend buscando en el navegador localhost:80

** En comandosSQL hay comandos para meter datos en las tablas de markers y measurements