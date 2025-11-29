# Documentación del Proyecto: Marketplace_Main

## Integrantes  
- Gamboa Cordova Jorge Dennis  
- Lejeune Alaniz Katheryne  
- Moreno Morales Adolfo  
- Villegas De La Cruz Aemee  

---

# Índice  
1. [Introducción](#introducción)  
2. [Comandos](#comandos)  
3. [Arquitectura MVT Django](#arquitectura-mvt-django)  
4. [Explicación de los archivos](#explicación-de-los-archivos)  
5. [Códigos](#códigos)  
6. [Ejecución del proyecto](#ejecución-de-lo-que-va-del-proyecto)  
7. [Conclusión](#conclusión)  

---

# Introducción  

## ¿Por qué utilizar Django para desarrollar aplicaciones web?

Django es un framework de desarrollo web basado en Python que permite crear aplicaciones de manera rápida, segura y eficiente. Su principales ventajas es que ofrece una estructura organizada para trabajar, lo que facilita mantener un código limpio y ordenado, contiene un lenguaje sencillo y entendible y comandos muy eficientes. Además, incluye muchas herramientas integradas que ayudan a los desarrolladores a enfocarse en la lógica de su aplicación sin preocuparse por tareas repetitivas.
Si buscas crear un proyecto, Django es una buena opción ya que el lenguaje es sencillo y solo tienes que seguir algunos pasos para crear tu proyecto, únicamente lo que necesitarás es tener conocimientos sobre Python.
Entre sus beneficios se encuentran su sistema de autenticación de usuarios, el panel de administración automático, la gestión de bases de datos y la posibilidad de manejar plantillas HTML para crear páginas dinámicas. En resumen, utilizar Django para desarrollar aplicaciones web es una excelente opción porque combina rapidez, seguridad y escalabilidad, permitiendo crear desde proyectos pequeños hasta plataformas web complejas de manera profesional y eficiente.

En conjunto, estas modificaciones demuestran cómo Django permite desarrollar aplicaciones web completas y escalables mediante una estructura ordenada, herramientas integradas y un flujo de trabajo claro que facilita tanto la lógica del servidor como la interfaz del usuario.


---

# Comandos
**CD Documents:** Principalmente, este comando que utilizamos al comenzar nuestro proyecto sirve para indicar la ruta donde se guardará el proyecto.

**MD:** MD sirve para crear una carpeta, la carpeta la puedes utilizar para lo que desees, pero una vez de haberla creado y querer entrar en ella tienes que hacer un cd nombre_de_carpeta.

**python -m venv venv:** Este comando sirve para crear un entorno virtual, el cual es como una carpeta aislada y tu puedes instalar librerías o archivos que necesites para tu proyecto.

**venv\Scripts\activate:**  Sirve para activar el entorno virtual una vez que creaste el entorno virtual y las librerías que instales se guardarán dentro de venv sin afectar al resto del sistema.

**pip install django:** Con el comando pip, pip es el gestor de paquetes de Python. install le indicas al sistema que instale en este caso django. 

**Dir:** Este comando sirve para ver los archivos que hay en el directorio.

**django-admin startproject:** Este comando sirve para crear las bases del proyecto que llevarás a cabo, más adelante tu puedes configurar tu página web/proyecto

**code .:** Con este comando abres visual studio desde cmd

**python manage.py runserver:** Sirve para iniciar el servidor del proyecto django, básicamente ejecutas el proyecto y puedes ver avances.

**python manage.py startapp store:** Con este comando creas una aplicación dentro del proyecto, que se llamara como tu le indiques en este caso store, y esa aplicación contendrá sus propios archivos para poder configurarlo.

**python manage.py createsuperuser:** Este comando sirve para crear un usuario con el cual podrás acceder al panel de administración de Django
(http://127.0.0.1:8000/admin) y administrar el sitio.

**python manage.py makemigrations:** Este comando tiene archivos de migración, e indica que tablas o columnas se tienen que modificar cuando tu lo indicas en el código.

**python manage.py migrate:** Este comando aplica las instrucciones de modificar una tabla o columna y actualiza la base de datos. Crea o modifica las tablas según los modelos de tu aplicación.

**pip freeze > requirements.txt:** Este comando crea un archivo que guarda todas las librerías que tienes instaladas en tu entorno virtual  Este archivo lo puedes:
-Usar tú mismo más adelante, si necesitas volver a instalar todo desde cero.
-Compartir con otras personas, para que puedan tener las mismas librerías en su entorno virtual.

### **Comandos nuevos**

**git clone :** Copiamos un repositorio remoto a nuestra computadora, creando una carpeta con todo el proyecto y su historial de cambios. Ejemplo: git clone https://github.com/usuario/proyecto.git

**git add . :** Cuando hacemos modificaciones, usamos git add . para preparar todos los archivos modificados y nuevos, diciéndole a Git que queremos incluirlos en el próximo commit. Para revisar qué archivos han cambiado o cuáles están listos para guardarse

**git status:** Usamos git status, que nos muestra el estado actual del repositorio.

**git commit -m:** Hacemos git commit -m "mensaje", que guarda esos cambios en el historial de Git con un mensaje que explique lo que hicimos.

**git push:** Con git push enviamos nuestros commits al repositorio remoto, para que los cambios queden reflejados en la nube y puedan ser vistos o usados por otros.
---
#Arquitectura MVT Django
![Texto alternativo](https://photos.google.com/album/AF1QipPt7dkI7cpF1wol2guFCE8U-PNiWe3RhRSLQz4K/photo/AF1QipNspUPmPKejhTZkXtvm1UxpuKRHQJw3PL06HG3n)

```bash
cd Documents
