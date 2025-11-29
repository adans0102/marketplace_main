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

**git push:** git push: Con git push enviamos nuestros commits al repositorio remoto, para que los cambios queden reflejados en la nube y puedan ser vistos o usados por otros.

---

# Arquitectura MVT Django
![mtv](https://photos.fife.usercontent.google.com/pw/AP1GczN8Nl-MmfkFRvjwP6cBF-nIZzOVYEZUjLoFgSPcFrikY4l16Ulrn6Wx=w1024-h768-s-no-gm?authuser=0)
Django separa el manejo de datos, la lógica y la presentación en tres partes:
El Modelo trabaja con la información, la Vista decide qué hacer con esa información y la Template (plantilla) se encarga de mostrarla al usuario. Así todo está organizado y es más fácil mantener el proyecto.

### **Cómo está ligado forms.py, views.py, signup.html y urls.py en la aplicación**
'store' del proyecto 'Marketplace _main'.**
Cuando entramos a /signup urls.py activa la vista correspondiente en views.py haciendo que carga el formulario definido en forms.py y decide si mostrarlo vacío o procesarlo cuando lo envíamos a signup.html haciendo que despliegue el formulario permitiendo que ingresemos datos y al enviarlo la información regresa a views.py para ser validada y guardada finalmente todo el flujo permite que el usuario se registre correctamente en el sistema sin necesidad de escribir SQL y manteniendo la
información organizada y segura

---
# Explicación de los archivos
___1.Settings.py:___ Este archivo es aquel que contiene toda la configuración de Django, en este se definen aspectos como:
Aplicaciones instaladas
La base de datos que se usa 
Rutas de archivos estáticos
Configuración de idioma y zona horaria

___2.urls.py :___ Este archivo define las rutas (URLs) del sitio web, es decir, qué vista (página o función) se muestra cuando el usuario entra a una dirección específica.

___3.models.py  :___ En este apartado se definen los modelos de datos, es decir, las tablas de la base de datos

___4.views.py :___ Aquí van las vistas, que son las funciones o clases que se ejecutan cuando un usuario visita una página.

___5.Folder template\store:___ Esta carpeta contiene los archivos HTML que se muestran en el navegador , los archivos dentro de template se combinan con los datos que las vistas envían y forman las páginas que el usuario ve.

### **Explicación de los archivos nuevos**

___1.Forms.py (LoginForm, SignupForm, NewItemForm)___

Este archivo se encarga de crear formularios personalizados que se usarán en la 
aplicación Django. Los formularios sirven para recibir datos del usuario, validarlos y enviarlos a las vistas o modelos. 

LoginForm: Personaliza el login de Django con campos de texto y contraseñas estilizados.


SignupForm: Crea nuevos usuarios con validación de contraseñas y campos bien  presentados.


NewItemForm: Permite añadir nuevos productos al marketplace, con campos bien  organizados  y estilizados para una mejor experiencia.

___2.Views.py (login(), logout_user(), detail(), add_item())___
En login(), el usuario ingresa sus datos y, si son correctos, se inicia su sesión.

logout_user() cierra la sesión y lo redirige.

detail() muestra la información completa de un producto según su ID.

add_item() muestra un formulario para crear un producto y lo guarda cuando es  válido.

___3.Explicar decorador @login_required___
El decorador @login_required se usa en Django para proteger una vista y permitir que solo los usuarios que han iniciado sesión puedan acceder a ella.
Si no lo está, Django lo manda automáticamente a la página de login.

___4.Urls.py__ (Las rutas a cada acción nueva en views)
En urls.py se añadieron las rutas que permiten acceder a cada una de las acciones creadas en views. Aquí se definen las URL que el usuario puede visitar y la vista que se ejecutará cuando lo haga.
Se agregó una ruta para login, que apunta a la vista encargada de iniciar sesión; otra para logout, que cierra la sesión del usuario; una ruta dinámica para detail, que recibe el ID del producto y muestra toda su información; y finalmente la ruta add_item, donde el usuario puede añadir un nuevo producto mediante el formulario.

___5.store/templates (item.html, login.html, signup.html, navigation.html, form.html)___
En la carpeta de templates se crearon las páginas que muestran al usuario la información del marketplace.
El archivo item.html se encargó de mostrar todos los detalles de un producto: su nombre, imagen, descripción y precio. Es la página que aparece cuando el usuario entra al detalle de un ítem.
En login.html y signup.html se diseñaron las pantallas donde el usuario puede iniciar sesión o crear una cuenta. Estas páginas muestran los formularios correspondientes y están estilizadas para que el proceso sea simple y claro.
El archivo navigation.html contiene el menú de navegación que aparece en la parte superior del sitio. Desde aquí el usuario puede moverse entre las distintas secciones, como inicio, login, logout o añadir un producto.
Por último, form.html sirve como plantilla genérica para mostrar formularios, como el de crear un ítem. Permite reutilizar el mismo diseño sin tener que repetir código.

```bash
