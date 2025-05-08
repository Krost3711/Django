# Django
Task Maintenance ⛑

This project will help you understand how mount an environment of Django, using Python language of programming, in order to get a Task Maintenance, where you will create, mark and delete your own tasks.

## What is required?
* Django
* Pycharm
* Python

## Steps to Follow
> Creamos un proyecto nuevo, este debe ser creado desde un ambiente virtual para no interferir con nuestro ambiente de desarrollo oficial.
> Seguidamente para efectos practicos, es necesario descargar los archivos necesarios de la apliacion, los cuales deben ser agregados al proyecto anteriomente creado, pero en el momento requerido, antes de esto es necesario configurar el mismo y crear el ambiente para que la aplicacion funcione correctamente.

## Paso 1: Instalacion de Django.
```sh
pip install django
```
## Paso 2: Configuracion del Proyecto.
Una vez creado el proyecto nuevo, creamos un directorio llamado src dentro del proyecto, nos dirigimos a el una vez creado y procedemos con el siguiente comando desde consola. (Aclaratoria: proyecto es el nombre de la carpeta, esta puede ser cambiada a preferencia)

```sh
django-admin startproject proyecto
```

Esto creara el archivo manage.py el cual es indispensabe para la configuracion y ejecucion del proyecto.

Seguidamente es necesario levantar el servidor, por lo que desde el terminal ejecutamos el siguiente comando, esto desde el directorio proyecto.

```sh
python manage.py runserver
```

Esto creara el archivo de base de datos db.sqlite3, y nos mostrara una direccion ip y puerto donde esta alojado nuestro servidor, seguidamente ejecutamos el siguiente comando para culminar con la configuracion.

```sh
python manage.py migrate
```

Y finalmente volvemos a ejecutar el comando, para que la configuracon anterior surja efecto.

```sh
python manage.py runserver
```

Para poder ingresar al modo administrador y crear un usuario es necesario ejecutar el siguiente comando, esto nos permitira ingresar al servidor brindandonos la opcion de crear un nuevo usuario.

```sh
python manage.py createsuperuser
```

Digitamos el nombre del usuario y un password de minimo 8 caracteres y volvemos a ejecutar el servicio con
```sh
python manage.py runserver
```
para guardar los cambios.

A la direccion ip le agregamos un /admin para entrar al administrador de base de datos, he ingresamos con el usuario anteriomente creado.

## Ultimos pasos, ya casi estamos terminando con la configuracion.

Luego ejecutamos el siguiente comando: 
```sh
python manage.py startapp base
```
. Esto creara un directorio nuevo llamado "base" dentro de nuestro proyecto indispensable para la ejecucion del mismo.

Ahora lo que vamos a realizar es la conexion entre el proyecto y la aplicacion. (En este caso 'base', directorio que esta vacio). Esto lo hacemos desde al archivo setting.py, en el directorio proyecto, agregando en el metodo
INSTALLED_APPS, la siguiente linea de codigo: 
```sh
'base.apps.BaseConfig',
```
Con esto ya se pueden conocer entre ellos.

## Paso 3: Realizamos un par de ultimas configuraciones.

*Creamos un nuevo archivo en la carpeta base, llamado urls.py

*Seguidamente importamos desde este ultimo archivo las siguientes librerias.

from django.urls import path

from . import views

*Luego en el archivo views, importamos la siguiente libreria from django.http import HttpResponse

*En el archivo urls de la carpeta proyecto importamos tambien include, esto deberia de quedar asi:

from django.urls import path, include

*Dentro de urlpatterns, debemos agregar path('',include('base.urls')),

## Paso 4: Copiamos los archivos de la carpeta templates que contine las interfaces.

*Para este paso debemos crear una carpeta templates en nuestra carpeta base y ahi copiar los archivos

*Y por ultimo debemos crear las tablas en la base de datos

EN PROCESO

Finalmente ejecutamos el siguiente comando:
```sh
python manage.py makemigrations
```
. Esto creara una carpeta llamada migrations que contendra la informacion de nuestras tablas para la base de datos.

Culminamos ejecutando el siguiente comando:
```sh
python manage.py migrate
```
. Y como es de costumbre ejecutamos el comando para refrescar nuestro servidor:
```sh
python manage.py runserver
```

De esta forma estariamos listos para ejecutar nuestra aplicacion desde Pycharm he ingresar a la aplicacion desde el navegador y gestionar la creacion de usuarios y creacion de tareas, segun corresponda.










