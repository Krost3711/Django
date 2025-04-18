# Django
Task Maintenance ⛑

This project will help you understand how mount an environment of Django, using Python language of programming, in order to get a Task Maintenance, where you will create, mark and delete your own tasks.

## What is required?
* Django
* Pycharm
* Python

## Steps to Follow
> Creamos un proyecto nuevo, este debe ser creado desde un ambiente virtual para no interferir con nuestro ambiente de desarrollo oficial.
> Seguidamente para efectos practicos, descargar los archivos necesario de la apliacion, los cuales deben ser agregados al proyecto anteriomente creado.

## Instalacion de Django
pip install django
## Configuracion del Proyecto
Luego creamos un directorio llamado src, nos dirigimos a el una vez creado y procedemos con el siguiente comando. (proyecto es el nombre de la carpeta, esta puede ser cambiada a preferencia)

django-admin startproject proyecto

Esto creara el archivo manage.py el cual es indispensabe para la configuracion y ejecucion del proyecto.

Seguidamente es necesario levantar e servidor por lo que desde e terminal ejecutamos el siguiente comando, desde el directorio proyecto

python manage.py runserver

Esto creara el archivo de base de datos db.sqlite3, y nos mostrara una direccion ip y puerto donde esta alojado nuestro servidor seguidamente ejecutamos el siguiente comando para culminar con la
configuracion.

python manage.py migrate

Y finalmente volvemos a ejecutar el comando

python manage.py runserver

Para poder ingresar al modo administrador y crear un usuario es necesario ejecutar el siguiente comando

python manage.py createsuperuser

Digitamos el nombre del usuario y un password de minimo 8 caracteres y volvemos a ejecutar el servicio con python manage.py runserver

A la direccion ip le agregamos un /admin para entrar al administrador de base de datos, he ingresamos con el usuario anteromente creado.






