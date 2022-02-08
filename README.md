# Plantilla de proyecto CGIS

Esta es una descripción por defecto de **ProyectoPrueba**. Aquí deberá aparecer la descripción que también aparezca en el documento


## Instrucciones para su uso
1. Desde Windows Terminal, si partimos desde el home del usuario `/~ o C:\Users\xxx` , iremos a la carpeta que contiene nuestro proyecto:
   `cd code/nombreproyecto`
2. Necesitamos un archivo de entorno `.env` para que nuestra aplicación sepa cómo conectarse a la base de datos y otros parámetros de configuración. Sin embargo, como el archivo `.env` contiene información sensible, como contraseñas, y la configuración depende del equipo, no se suele subir al repositorio (poniendo en `.gitignore` el archivo para que Git no lo considere). En su lugar, hemos subido un ejemplo `.env.example` con valores de ejemplo para los diferentes parámetros. En este caso, los valores de ejemplo son exactamente los mismos que necesitamos para trabajar con sail, así que tendremos que duplicar el archivo `.env.example`, copiándolo y pegándolo en el mismo directorio, y llamándolo `.env`

3. Arrancamos el contenedor de Sail `./vendor/bin/sail up -d`

4. Abrimos VSCode `code .`

5. Abrimos un terminal al contenedor de Sail para ejecutar comandos.

6. Cuando descargas el repositorio, todas las dependencias de nuestro proyecto (todo el código que no hemos desarrollado nosotros pero que necsitamos, como el framework de Laravel, Carbon para la gestión de fechas, etc.) no están disponibles.
Para ello, desde Windows Terminal, ejecutaremos `composer install` dentro de la carpeta de nuestro repositorio.

7. Abre en el navegador `http://localhost`


## Herramienta para escribir lenguaje de marcado
https://www.markdownguide.org/basic-syntax/ describe cómo se utiliza el markdown.

[StackEdit](https://stackedit.io/app#) puede ayudaros a trabajar con lenguajes de marca (markdown) para escribir este README.md
> Prueba las posibilidades antes de **Subir** cambios al repositorio.




