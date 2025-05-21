# Instalación

## Requerimientos

Tener instalado Node.JS (De preferencia la version LTS)

Tener instalada la ultima versión de XAMPP o un servidor local equivalente.

Revisa la lista de requerimientos de laravel [Check Laravel Requirement](https://laravel.com/docs/10.x/deployment#server-requirements)

### Clonar el repositorio

    git clone https://github.com/angkosal/laravel-pos.git [YourDirectoryName]

### Instalar las Dependencias

Laravel utilizes [Composer](https://getcomposer.org/) para poder orquestar de manera correcta las dependencias de PHP, y sus versiones ademas de los pluggins

    cd YourDirectoryName
    composer install

### Variables de Entorno

1. Establece tus variables de base de datos en el archivo `.env`
1. Agrega las variables de entorno locales necesarias en en archivo `.env`

### Generar llave para la app
 
 1.`php artisan key:generate` 

### Base de datos

1. Migrar las tablas de la base de datos `php artisan migrate`

Este comando inicializará, creará y configurará el usuadio admin cuyas credenciales iniciales son: [email: admin@gmail.com - password: admin123]

1. `php artisan db:seed`

De igual manera puedes iniciar sesión gracias a las capacidades de laravel breeze

### Instalar las dependencias de Node.js

1. `npm install` to install node dependencies
2. `npm run dev` for development or `npm run build` for production (A pesar que no se implementase en producción recomiendo altamente correr las herramientas de desarrollo de Node.js)

### Crear la conexión con la base de datos

`php artisan storage:link`

### Correr el server de manera local

Incicial el servidor:

```
php artisan serve
```
En tu navegador accede a:

**http://localhost:8000/**
