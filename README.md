# Plantilla de proyecto CGIS

Esta es una descripción por defecto de **ProyectoPrueba**. Aquí deberá aparecer la descripción que también aparezca en el documento


## Instrucciones para su uso
1. Desde Windows Terminal, si partimos desde el home del usuario `/~ o C:\Users\xxx` , iremos a la carpeta que contiene nuestro proyecto:
   `cd code/nombreproyecto`
2. Necesitamos un archivo de entorno `.env` para que nuestra aplicación sepa cómo conectarse a la base de datos y otros parámetros de configuración. Sin embargo, como el archivo `.env` contiene información sensible, como contraseñas, y la configuración depende del equipo, no se suele subir al repositorio (poniendo en `.gitignore` el archivo para que Git no lo considere). En su lugar, hemos subido un ejemplo `.env.example` con valores de ejemplo para los diferentes parámetros. En este caso, los valores de ejemplo son exactamente los mismos que necesitamos para trabajar con sail, así que tendremos que duplicar el archivo `.env.example`, copiándolo y pegándolo en el mismo directorio, y llamándolo `.env`

3. Arrancamos el contenedor de Sail por primera vez `docker-compose up -d`

4. Abrimos un terminal al contenedor de Sail para ejecutar comandos.

5. Cuando descargas el repositorio, todas las dependencias de nuestro proyecto (todo el código que no hemos desarrollado nosotros pero que necsitamos, como el framework de Laravel, Carbon para la gestión de fechas, etc.) no están disponibles.
Para ello, desde el Terminal asociado al contenedor, ejecutaremos `composer install` dentro de la carpeta de nuestro repositorio.

6. Ahora que tenemos disponible la carpeta disponible de vendor, podemos gestionar el contenedor de forma ordinaria. Para ello, vaya de nuevo a Window Terminal (el terminal de la máquina Host, no la asociada con el contenedor Docker de Sail) y apague el contenedor `docker-compose down`
 
7. Y levántela de nuevo desde Window Terminal (el terminal de la máquina Host, no la asociada con el contenedor Docker de Sail), pero esta vez gestionada por Sail `./vendor/bin/sail up -d`

8. Abrimos VSCode desde Window Terminal `code .`

9. Abre en el navegador `http://localhost`

**IMPORTANTE** Tendrá dos terminales: 1 ataca a la máquina física y otro al contenedor. Los comandos como `php artisan xxx`, `composer xxx`, siempre serán ejecutados sobre el contenedor, ya que necesitan el entorno de desarrollo con MySQL, PHP, etc. (contenedor), mientras que la gestión del contenedor, como `./vendor/bin/sail up -d` o `./vendor/bin/sail down`, desde la máquina física.

## Herramienta para escribir lenguaje de marcado
https://www.markdownguide.org/basic-syntax/ describe cómo se utiliza el markdown.

[StackEdit](https://stackedit.io/app#) puede ayudaros a trabajar con lenguajes de marca (markdown) para escribir este README.md
> Prueba las posibilidades antes de **Subir** cambios al repositorio.




