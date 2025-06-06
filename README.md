# SharkEnergy

![Logo](/logo/SharkEnergy.jpeg)

---

# Capturas de Pantalla

### Inicio de Sesión

![Login del Sistema](/screenshots/Login.PNG)

### Dashboard

![Inicio](/screenshots/DashBoard.PNG)

### Clientes

![Tabla de Clientes](/screenshots/Clientes.PNG)

### Proveedores

![Tabla de Proveedores](/screenshots/Proveedores.PNG)

### Productos

![Tabla de Productos](/screenshots/Productos.PNG)

### Punto de Venta

![Punto de Venta](/screenshots/PuntoVenta.PNG)

### Ordenes

![Ordenes](/screenshots/Ordenes.PNG)

### Inicialización del Contenedor

![Docker](/screenshots/LoadingDocker.PNG)

# Documentacion

Para acceder a la configuración completa accede a la carpeta 

> Documentation

---

# Instalación

### Requerimientos

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

---

## Descripcion de la Problematica

Un familiar de uno de los integrantes de este equipo, se comunicó con nosotros para solicitarnos un sistema de gestión de Inventario y una página web, pues estaba arreglando todo para poder abrir un negocio de calentadores solares y paneles solares.

Nos reunimos con la persona y hablando llegamos a la conclusión de que lo mejor sería tener un sistema gestor de ventas, pero él nos solicitó que quería un sistema de punto de vista con gestión de inventario y que fuera independiente de la página web.

No es la solución más elegante pero eso fue lo que nos solicitó, muchas de las cosas que pareciese mal diseñadas están de esa manera por solicitud de la persona que nos contactó.

## Alcances

Gestión de inventario: El sistema permitirá registrar, organizar y administrar los productos en existencia, así como realizar un seguimiento de las entradas y salidas de inventario.

Sistema de punto de venta (POS): Se implementará una herramienta que facilite la realización de transacciones de venta, con funcionalidad para calcular totales, generar comprobantes y registrar ventas realizadas.

Independencia del sistema: El sistema funcionará de manera local, sin depender de la página web del negocio.

Personalización según las necesidades del cliente: El diseño y las funcionalidades estarán adaptados a los requerimientos específicos del negocio de calentadores solares y paneles solares.

Interfaz sencilla e intuitiva: Se desarrollará una interfaz amigable para el administrador, asegurando un uso eficiente y accesible.

Compatibilidad local: El sistema estará diseñado para operar en el estado de Jalisco, considerando las particularidades de mercado y las necesidades locales.

## Limitaciones

Operación local: El sistema funcionará exclusivamente de manera local, sin opciones de acceso remoto o sincronización en línea.

Cobertura geográfica limitada: Por el momento, el sistema está diseñado para ser implementado únicamente en negocios dentro del estado de Jalisco.

Falta de roles de usuario: El sistema no manejará diferentes tipos de usuarios, limitándose a un único perfil de administrador para todas las operaciones.

Dependencia de hardware local: El sistema requerirá hardware específico (computador o dispositivo local) para su instalación y operación, sin opciones de acceso desde otros dispositivos o plataformas.

Sin integración con otros sistemas: No se contempla la integración con otros sistemas externos, como plataformas de e-commerce, servicios contables o herramientas de análisis.

## Metodología

Para el desarrollo del sistema Shark Energy, se utilizó la metodología ágil. Esta metodología fue seleccionada debido a su enfoque iterativo y flexible, lo que permitió adaptarnos a los requerimientos específicos del cliente y realizar ajustes continuos durante el proceso de desarrollo. La naturaleza dinámica del proyecto, así como las solicitudes específicas del cliente, hicieron de este enfoque la mejor opción para garantizar un resultado satisfactorio.

El desarrollo se llevó a cabo en ciclos iterativos, denominados sprints, que incluyeron las siguientes etapas clave:

Planificación inicial: En esta etapa, se definieron los objetivos generales del proyecto y se priorizaron las funcionalidades principales, como la gestión de inventario y el sistema de punto de venta. También se estableció una lista inicial de tareas y entregables.

Desarrollo iterativo: Durante cada sprint, se trabajó en la implementación de funcionalidades específicas. Al final de cada ciclo, se entregaron incrementos funcionales del sistema, los cuales fueron evaluados por el cliente para recibir retroalimentación.

Revisión y retroalimentación constante: Una de las ventajas de la metodología ágil es la comunicación continua con el cliente. Esto permitió realizar ajustes en tiempo real, adaptando el sistema a las necesidades cambiantes del negocio y asegurando que las solicitudes específicas fueran cumplidas.

Pruebas continuas: A lo largo de cada sprint, se realizaron pruebas en las funcionalidades desarrolladas para garantizar su correcto funcionamiento. Esto incluyó pruebas de las transacciones de venta, el manejo de inventarios y la estabilidad general del sistema.

---

### Software Utilizado para la Creación de este proyecto

![Laravel](/requirments/laravel.png)

![Node.JS](/requirments/NodeJS.png)

![XAMPP](/requirments/XAMPP.jpg)

![Docker](/requirments/docker.png)

## Importancia de Docker en un proyecto web

1. Docker encapsula tu aplicación y todas sus dependencias en contenedores. Esto significa que el entorno de desarrollo, pruebas y producción será exactamente el mismo, sin importar dónde se ejecute (tu máquina local, un servidor en la nube, etc.). Esto elimina los problemas de "funciona en mi máquina, pero no en el servidor".

Ejemplo: Si tu proyecto Laravel depende de una versión específica de PHP o MySQL, Docker garantiza que esas versiones estarán disponibles en cualquier entorno.

2. Facilidad de configuración
Con Docker, puedes definir todo el entorno necesario (como PHP, MySQL, Redis, etc.) en un archivo docker-compose.yml. Esto simplifica la configuración y evita tener que instalar manualmente herramientas como XAMPP o configurar servidores locales.

Ejemplo: En lugar de instalar MySQL en tu máquina y configurarlo para que funcione con Laravel, simplemente defines un servicio de base de datos en Docker y todo estará listo.

3. Aislamiento de entornos
Cada contenedor de Docker es independiente y está aislado del sistema operativo anfitrión y de otros contenedores. Esto significa que puedes tener múltiples proyectos con diferentes configuraciones ejecutándose al mismo tiempo sin conflictos.

Ejemplo: Si tienes un proyecto Laravel que usa PHP 8.1 y otro que usa PHP 7.4, puedes ejecutar ambos en contenedores separados sin problemas.

4. Escalabilidad
Docker facilita la escalabilidad de aplicaciones. Si necesitas más instancias de tu aplicación o servicios adicionales (como balanceadores de carga), puedes configurarlos fácilmente en Docker y desplegarlos en un clúster.

Ejemplo: Si tu proyecto Laravel crece y necesitas manejar más tráfico, puedes escalar horizontalmente agregando más contenedores de tu aplicación.

5. Fácil integración con herramientas modernas
Docker se integra perfectamente con herramientas y servicios modernos como Kubernetes, CI/CD (Integración y Despliegue Continuo), y sistemas de monitoreo. Esto mejora la productividad y la capacidad de desplegar aplicaciones rápidamente.

Ejemplo: Puedes usar Docker en un pipeline de CI/CD para probar y desplegar tu aplicación Laravel automáticamente en cada cambio de código.

6. Estandarización
Docker promueve la estandarización de los entornos de desarrollo. Todo el equipo de desarrollo trabajará en el mismo entorno, lo que reduce errores y discrepancias.

Ejemplo: Si un miembro del equipo usa Windows y otro usa macOS, ambos tendrán el mismo entorno de desarrollo gracias a Docker.

7. Reducción de problemas de configuración
Configurar manualmente un entorno de desarrollo con herramientas como XAMPP puede ser propenso a errores y consumir mucho tiempo. Docker automatiza esta configuración y asegura que todo esté correctamente configurado.

Ejemplo: No tendrás que preocuparte por instalar extensiones de PHP o configurar puertos manualmente; Docker lo hace por ti.

8. Despliegue simplificado
Con Docker, puedes empaquetar tu aplicación y desplegarla fácilmente en cualquier servidor que soporte Docker. Esto elimina la necesidad de configurar servidores manualmente.

Ejemplo: Puedes construir una imagen de Docker para tu proyecto Laravel y desplegarla en servicios como AWS, Google Cloud o Azure con unos pocos comandos.

9. Compatibilidad con múltiples servicios
Proyectos como Laravel suelen requerir múltiples servicios (como bases de datos, colas de trabajo, almacenamiento en caché, etc.). Docker permite configurar y ejecutar todos estos servicios fácilmente en contenedores.

Ejemplo: Puedes configurar MySQL, Redis y Laravel Horizon en un solo archivo docker-compose.yml y ejecutarlos juntos.

10. Reducción de costos
Al usar Docker, puedes reducir los costos asociados con la configuración y mantenimiento de entornos de desarrollo y producción. Además, Docker utiliza los recursos del sistema de manera más eficiente que las máquinas virtuales tradicionales.

