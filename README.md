# Documentación del Proyecto: Marketplace_Main

## Integrantes  
- Gamboa Cordova Jorge Dennis  
- Lejeune Alaniz Katheryne  
- Moreno Morales Adolfo  
- Villegas De La Cruz Aemee
- Sánchez Sánchez Aylin Daniela

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
![MTV](https://drive.google.com/uc?export=view&id=1M3KJGMKy2ko25Gwp6x_DMg7hEdP7UmAZ)
Django separa el manejo de datos, la lógica y la presentación en tres partes:
El Modelo trabaja con la información, la Vista decide qué hacer con esa información y la Template (plantilla) se encarga de mostrarla al usuario. Así todo está organizado y es más fácil mantener el proyecto.

### **Cómo está ligado forms.py, views.py, signup.html y urls.py en la aplicación**
![relacionentrelosarchivos](https://drive.google.com/uc?export=view&id=1eNGYATxhF-Kway4hqr0-I4RgagttnC6i)

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

___1.Forms.py (LoginForm, SignupForm, NewItemForm): ___ Este archivo se encarga de crear formularios personalizados que se usarán en la 
aplicación Django. Los formularios sirven para recibir datos del usuario, validarlos y enviarlos a las vistas o modelos. 

LoginForm: Personaliza el login de Django con campos de texto y contraseñas estilizados.

SignupForm: Crea nuevos usuarios con validación de contraseñas y campos bien  presentados.

NewItemForm: Permite añadir nuevos productos al marketplace, con campos bien  organizados  y estilizados para una mejor experiencia.

___2.Views.py (login(), logout_user(), detail(), add_item()):___
En login(), el usuario ingresa sus datos y, si son correctos, se inicia su sesión.

logout_user() cierra la sesión y lo redirige.

detail() muestra la información completa de un producto según su ID.

add_item() muestra un formulario para crear un producto y lo guarda cuando es  válido.

___3.Explicar decorador @login_required:___
El decorador @login_required se usa en Django para proteger una vista y permitir que solo los usuarios que han iniciado sesión puedan acceder a ella.
Si no lo está, Django lo manda automáticamente a la página de login.

__4.Urls.py (Las rutas a cada acción nueva en views):___ En urls.py se añadieron las rutas que permiten acceder a cada una de las acciones creadas en views. Aquí se definen las URL que el usuario puede visitar y la vista que se ejecutará cuando lo haga.
Se agregó una ruta para login, que apunta a la vista encargada de iniciar sesión; otra para logout, que cierra la sesión del usuario; una ruta dinámica para detail, que recibe el ID del producto y muestra toda su información; y finalmente la ruta add_item, donde el usuario puede añadir un nuevo producto mediante el formulario.

___5.store/templates (item.html, login.html, signup.html, navigation.html, form.html):___ En la carpeta de templates se crearon las páginas que muestran al usuario la información del marketplace.
El archivo item.html se encargó de mostrar todos los detalles de un producto: su nombre, imagen, descripción y precio. Es la página que aparece cuando el usuario entra al detalle de un ítem.
En login.html y signup.html se diseñaron las pantallas donde el usuario puede iniciar sesión o crear una cuenta. Estas páginas muestran los formularios correspondientes y están estilizadas para que el proceso sea simple y claro.
El archivo navigation.html contiene el menú de navegación que aparece en la parte superior del sitio. Desde aquí el usuario puede moverse entre las distintas secciones, como inicio, login, logout o añadir un producto.
Por último, form.html sirve como plantilla genérica para mostrar formularios, como el de crear un ítem. Permite reutilizar el mismo diseño sin tener que repetir código.

---

# Códigos
___1. Settings.py:___
```
"""
Django settings for marketplace_main project.


Generated by 'django-admin startproject' using Django 5.2.7.


For more information on this file, see
https://docs.djangoproject.com/en/5.2/topics/settings/


For the full list of settings and their values, see
https://docs.djangoproject.com/en/5.2/ref/settings/
"""


from pathlib import Path


# Build paths inside the project like this: BASE_DIR / 'subdir'.
BASE_DIR = Path(__file__).resolve().parent.parent




# Quick-start development settings - unsuitable for production
# See https://docs.djangoproject.com/en/5.2/howto/deployment/checklist/


# SECURITY WARNING: keep the secret key used in production secret!
SECRET_KEY = 'django-insecure-ds$4fw+x@!y9v_-b#x5p!jamy)4yjbz2jt8-=rz-0y#v@+g($l'


# SECURITY WARNING: don't run with debug turned on in production!
DEBUG = True


ALLOWED_HOSTS = []




# Application definition


INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'store',
]


MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',


   
]


ROOT_URLCONF = 'marketplace_main.urls'


TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]


WSGI_APPLICATION = 'marketplace_main.wsgi.application'




# Database
# https://docs.djangoproject.com/en/5.2/ref/settings/#databases


DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}




# Password validation
# https://docs.djangoproject.com/en/5.2/ref/settings/#auth-password-validators


AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
    },
]




# Internationalization
# https://docs.djangoproject.com/en/5.2/topics/i18n/


LANGUAGE_CODE = 'en-us'


TIME_ZONE = 'UTC'


USE_I18N = True


USE_TZ = True




# Static files (CSS, JavaScript, Images)
# https://docs.djangoproject.com/en/5.2/howto/static-files/


STATIC_URL = 'static/'
MEDIA_URL ='media/'
MEDIA_ROOT= BASE_DIR / 'media'


# Default primary key field type
# https://docs.djangoproject.com/en/5.2/ref/settings/#default-auto-field


DEFAULT_AUTO_FIELD = 'django.db.models.BigAutoField'
```

___2.Urls.py:___
```
from django.contrib import admin
from django.urls import path
from django.conf import settings
from django.conf.urls.static import static
from store.views import home
```

___3.Models.py:___
```
from django.contrib.auth.models import User
from django.db import models




# Create your models here.
class Category(models.Model):
    name= models.CharField(max_length=255)




    class Meta:
        ordering = ('name',)
        verbose_name_plural = 'Categories'




    def __str__(self):
        return self.name
       
class  Item(models.Model):
    category = models.ForeignKey(Category, related_name = 'items', on_delete=models.CASCADE)
    name = models.CharField(max_length=255)
    description = models.TextField(blank=True, null=True)
    price = models.FloatField()
    image = models.ImageField(upload_to='item_images', blank=True, null=True)
    is_sold = models.BooleanField(default=False)
    created_by= models.ForeignKey(User, related_name='items', on_delete=models.CASCADE)
    created_at = models.DateTimeField(auto_now_add=True)




    def __str__(self):
        return self.name



urlpatterns = [
    path('', home, name='home'),
    path('admin/', admin.site.urls),
] + static(settings.MEDIA_URL,document_root=settings.MEDIA_ROOT)
```

___4.views.py:___
```
from django.shortcuts import render
from .models import Item, Category
from django.shortcuts import get_object_or_404




# Create your views here.
def home (request):
    items = Item.objects.filter(is_sold=False)
    categories = Category.objects.all()




    context = {
        'items': items,
        'categories': categories
    }
    return render(request, 'store/home.html', context)
```

**5.Templates\store:**
___Código base.html:___
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-sRIl4kxILFvY47J16cr9ZwB07vP4J8+LH7qKQnuqkuIAvNWLzeN8tE5YBujZqJLB" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/js/bootstrap.bundle.min.js" integrity="sha384-FKyoEForCGlyvwx9Hj09JcYn3nv7wiPVlz7YYwJrWVcXK/BmnVDxM+D2scQbITxI" crossorigin="anonymous"></script>
    <title>{% block title %} {% endblock %} Market place</title>
</head>
<body>
    <section class="container">
        {% block content%}
        {% endblock %}
    </section>




    <footer class="py-5 text-center text-body-secondary bg-body-tertiary">
        <p>Copyright (c) - Marketplace by K. Lejeune Alaniz </p>
    </footer>








</body>
</html>
```

___Código home.html:___
```
{% extends 'store/base.html' %}




{% block title %}Home |{% endblock %}




{% block content %}
<div class="mt-2 mb-4 px-4 py-2">
    <h1 class="text-center mb-4">
        Nuevos Productos
    </h1>
    <div class="container text-center">
        <div class="row justify-content-center">
            {% for item in items %}
                <div class="col-xs-12 col-sm-6 col-md-6 col-lg-6 col-xl-3">
                    <div class="card" style="width: 18rem">
                        <img src="{{ item.image.url }}" class="card-img-top">
                        <div class="card-body">
                            <h5 class="card-title">{{ item.name }} - {{item.price}}</h5>
                            <p class="card-text">{{item.description}}</p>
                            <a href="#" class="btn btn-primary">Mas Detalles...</a>
                        </div>
                    </div>
                </div>
            {% endfor %}
        </div>
    </div>
</div>
{% endblock %}
```

### **Códigos nuevos**
**1.Store:**
___Forms.py:___
```
from django import forms
from django.contrib.auth.forms import UserCreationForm, AuthenticationForm
from django.contrib.auth.models import User

from .models import Item

class LoginForm(AuthenticationForm):
    username = forms.CharField(widget=forms.TextInput(
        attrs={
            'placeholder': 'Tu username',
            'class': 'form-control'
        }
    ))

    password = forms.CharField(widget=forms.PasswordInput(
        attrs={
            'placeholder': 'Tu password',
            'class': 'form-control'
        }
    ))

class SignupForm(UserCreationForm):
    class Meta:
        model = User
        fields = ['username', 'email', 'password1', 'password2' ]

    username = forms.CharField(widget=forms.TextInput(
        attrs={
            'placeholder': 'Tu Username',
            'class': 'form-control'
        }
    ))

    email = forms.CharField(widget=forms.EmailInput(
        attrs={
            'placeholder': 'Tu Email',
            'class': 'form-control'
        }
    ))

    password1 = forms.CharField(widget=forms.PasswordInput(
        attrs={
            'placeholder': 'Password',
            'class': 'form-control'
        }
    ))

    password2 = forms.CharField(widget=forms.PasswordInput(
        attrs={
            'placeholder': 'Repite Tu Password',
            'class': 'form-control'
        }
    ))

class NewItemForm(forms.ModelForm):
    class Meta:
        model = Item
        fields = ['category', 'name', 'description', 'price', 'image']
            
        widgets = {
            'category': forms.Select(
                attrs={
                    'class': 'form-select'
                }
            ),
            'name': forms.TextInput(
                attrs={
                    'class': 'form-select'
                }
            ),
            'description': forms.Textarea(
                attrs={
                    'class': 'form-select',
                    'style': 'height: 100px'
                }
            ),
            'price': forms.TextInput(
                attrs={
                'class': 'form-select'
                }
            ),
            'image': forms.FileInput(
                attrs={
                    'class': 'form-select'
                }
            )  
                
        }
```

___Views.py:___ 
```
from django.shortcuts import render, get_object_or_404, redirect
from django.contrib.auth import logout
from django.contrib.auth.decorators import login_required
from .models import Item, Category

from .forms import SignupForm, NewItemForm
 

# Create your views here.
def home(request):
    items = Item.objects.filter(is_sold=False)
    categories = Category.objects.all()

    context = {
        'items': items,
        'categories': categories
    }
    return render(request, 'store/home.html', context)

def contact(request):
    context = {
        'msg': 'Quieres otros productos contactame!'
    }

    return render(request, 'store/contact.html', context)

def detail(request, pk):
    item = get_object_or_404(Item, pk=pk)
    related_items = Item.objects.filter(category=item.category, 
                                        is_sold=False).exclude(pk=pk)[0:3]

    context={
        'item': item,
        'related_items': related_items
    }

    return render(request, 'store/item.html', context)

def register(request):
    if request.method == 'POST':
        form = SignupForm(request.POST)

        if form.is_valid():
            form.save()
            return redirect('login')
    else:
        form = SignupForm()
    
    context = {
        'form': form
    }

    return render(request, 'store/signup.html', context)

def logout_user(request):
    logout(request)

    return redirect('home')


@login_required
def add_item(request):
    if request.method == 'POST':
        form = NewItemForm(request.POST, request.FILES)

        if form.is_valid():
            item = form.save(commit=False)
            item.created_by = request.user
            item.save()

            return redirect('detail', pk=item.id)
    else:
        form = NewItemForm()
        context = {
            'form': form,
            'title': 'New Item'
        }

 return render(request, 'store/form.html', context)
```

**@login_required:**
```
@login_required
def add_item(request):
    if request.method == 'POST':
        form = NewItemForm(request.POST, request.FILES)

        if form.is_valid():
            item = form.save(commit=False)
            item.created_by = request.user
            item.save()

            return redirect('detail', pk=item.id)
    else:
        form = NewItemForm()
        context = {
            'form': form,
            'title': 'New Item'
        }

    return render(request, 'store/form.html', context)
```

___Urls.py:___
```
from django.urls import path
from django.contrib.auth import views as auth_views

from .views import contact, detail, register, logout_user, add_item

from .forms import LoginForm

urlpatterns = [
    path('contact/', contact, name='contact'),
    path('register/', register, name='register'),
    path('login/', auth_views.LoginView.as_view(template_name='store/login.html', authentication_form=LoginForm), name='login'),
    path('logout/', logout_user, name='logout'),
    path('add_item/', add_item, name='add_item'),
    path('detail/<int:pk>/', detail, name='detail'),
]
```

**2.store/templates:**
___item.html___
```
{% extends 'store/base.html' %}

{% block title %}{{item.name}} | {% endblock %}

{% block content %}
<div class="container mt-4 mb-4">
    <div class="row">
        <div class="col-4">
            <img src="{{ item.image.url }}" alt="" 
            class="rounded" width="100%"> 
        </div>
        <div class="col-8 p-4 rounded bg-light">
            <h1 class="mb-4 text-center">
                {{ item.name }}
            </h1>
            <hr>
            <h4><strong>Precio ${{ item.price }}</strong></h4>
            <h4><strong>Vendedor {{ item.created_by.username }}</strong></h4>
            
            {% if item.description %}
                <p>{{ item.description }}</p>
            {% endif %}

            <a href="" class="btn btn-dark">Contacta a el vendedor</a>
            
        </div>
    </div>
</div>
{% endblock %}
```

 ___login.html___
 ```
{% extends 'store/base.html' %}

{% block title %}Login| {% endblock %}

{% block content %}

<div class="row p-4 d-flex justify-content-center align-items-center">
    <div class="col-6 bg-light p-4">
        <h4 class="mb-6 text-center">Registro</h4>
        <hr>
        <form action="." method="POST">
            {% csrf_token %}
            <div class="form-floating mb-3">
                <h6>Username:</h6>
                {{form.username}}
            </div>
            <div class="form-floating mb-3">
                <h6>Password:</h6>
                {{form.password}}
            </div>


            {% if form.errors or form.non_field_errors %}
            <div class="mb-4 p-6 bg-danger text-white rounded">
                {% for field in form %}
                field.errors
                {% endfor %}
                {{ form.non_field_errors }}
            </div>
            {% endif %}
            <div class="d-flex justify-content-center align-items-center">
                <button class="btn btn-primary mb-6">Login</button>
            </div>
            <div class="d-flex justify-content-center align-items-center">
                <a href="{% url 'register' %}">¿No tienes cuenta? registrate aqui!</a>
            </div>
        </form>
    </div>
</div>



{% endblock %}
```

___signup.html___
```
{% extends 'store/base.html' %}

{% block title %}Registro| {% endblock %}

{% block content %}
<div class="row p-4 d-flex justify-content-center align-items-center">
    <div class="col-6 bg-light p-4">
        <h4 class="mb-6 text-center">Registro</h4>
        <hr>
        <form action="." method="POST">
            {% csrf_token %}
            <div class="form-floating mb-3">
                <h6>Username:</h6>
                {{form.username}}
            </div>
            <div class="form-floating mb-3">
                <h6>Email:</h6>
                {{form.email}}
            </div>
            <div class="form-floating mb-3">
                <h6>Password:</h6>
                {{form.password1}}
            </div>
            <div class="form-floating mb-3">
                <h6>Repite Password:</h6>
                {{form.password2}}
            </div>

            {% if form.errors or form.non_field_errors %}
                <div class="mb-4 p-6 bg-danger rounded">
                    {% for field in form %}
                        <h5 class="text-white">
                            {{field.errors}}
                        </h5>
                        
                    {% endfor %}
                    {{ form.non_field_errors }}
                </div>
            {% endif %}

            <div class="d-flex justify-content-center align-items-center">
                <button class="btn btn-primary mb-6">Register</button>
            </div>
            <div class="d-flex justify-content-center align-items-center">
                <a href="{% url 'login' %}">¿Ya tienes cuenta? Accesa aqui!</a>
            </div>
        </form>
    </div>
</div>
{% endblock %}s
```

___navigation.html___
```
<nav class="navbar navbar-expand-lg bg-dark" data-bs-theme="dark">
    <div class="container-fluid">
        <a href="{% url 'home' %}" class="navbar-brand">Marketplace</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-control="navBarNav" aria-expanded="false" aria-label="Toggle Navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item">
                    <a href="" class="nav-link active">
                        Home
                    </a>
                </li>
                <li class="nav-item">
                    <a href="{% url 'contact' %}" class="nav-link active">
                        Contact
                    </a>
                </li>
            
                {% if request.user.is_authenticated %}
                <li class="nav-item">
                    <a href="{% url 'add_item' %}" class="nav-link">Add Item</a>
                </li>
                    <li class="nav-item">
                        <a href="{% url 'logout' %}" class="nav-link">Logout</a>
                    </li>
                {% else %}
                    <li class="nav-item">
                        <a href="{% url 'login' %}" class="nav-link active">
                            Login
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="{% url 'register' %}" class="nav-link active">
                            Register
                        </a>
                    </li>

                {% endif %}
            </ul>
        </div>
    </div>
</nav>
```

___form.html___
```
{% extends 'store/base.html' %}

{% block title %}{{ title }} | {% endblock %}

{% block content %}
    <h4 class="mb-4-mt-4">{{ title }}</h4>
    <hr>
    <form action="." method="POST" enctype="multipart/form-data">
    {% csrf_token %}

    <div>
        {{ form.as_p }}
    </div>
    {% if form.errors or form.non_field_errors %}
                <div class="mb-4 p-6 bg-danger">
                    {% for field in form %}
                    <h5 class="text-white">
                        {{field.errors}}
                    </h5>
                    {% endfor %}

                    {{ form.non_field_errors }}
                </div>
    {% endif %}

    <button class="btn btn-primary mb-6">
        Add Item
    </button>
</form>
{% endblock %}
```

---

# Ejecución de lo que va del proyecto
![foto 1](https://drive.google.com/uc?export=view&id=1ejKmYitt0D9Tn0ha_ma33UFpGTvhQ9nk)

### **Ejecución actualizada**

![foto2](https://drive.google.com/uc?export=view&id=1lIxapwXw1BZ7H9qOcsRydRI1tWLamJ_1)
![foto3](https://drive.google.com/uc?export=view&id=1GKb_SG667Pci-dVCySLGJdv9EUfi4eCP)
![foto4](https://drive.google.com/uc?export=view&id=11IhE4DcMQkmNBTRgGMACR-g7dEZ2qst8)
![foto5](https://drive.google.com/uc?export=view&id=1-6GU3ISwH1FhDQzU749fygnL_3pbnEaz)
![foto6](https://drive.google.com/uc?export=view&id=1eWCbbHP18RSuQWal3-X3HplstbCsqtAt)
![foto7](https://drive.google.com/uc?export=view&id=1SyKBnRPLtcZUzLPV0U41sHzCWedMwRKG)
![foto8](https://drive.google.com/uc?export=view&id=1rcsHFa3pM2PF4XqTaMOPfw0RTfHsocYY)

---

# Conclusión

Venimos trabajando en este proyecto desde principios del parcial, y a lo largo de cada clase fuimos avanzando y aprendiendo más sobre el funcionamiento del framework Django y el desarrollo de aplicaciones web. Desde los primeros pasos, en los que configuramos el entorno virtual y el servidor local, hasta la creación de modelos, vistas y plantillas, el trabajo fue evolucionando clase a clase.
El proyecto Marketplace tuvo como objetivo crear una plataforma sencilla para mostrar productos con sus precios e imágenes, organizados por categorías. En el archivo settings.py configuramos la estructura base del proyecto, la base de datos y las rutas para manejar imágenes mediante la librería Pillow. En urls.py definimos las rutas principales, conectando la página de inicio y el panel de administración.
En models.py desarrollamos los modelos Category e Item, representando las categorías y los productos con campos como nombre, descripción, precio e imagen. Estos modelos fueron registrados en admin.py, lo que nos permitió administrar toda la información desde el panel de administración de Django, agregando y editando productos de forma visual y sencilla.
La vista home en views.py se encargó de mostrar los productos disponibles y las categorías en la página principal, conectando así la base de datos con el diseño visual del sitio. Gracias a esto, pudimos visualizar los productos, precios e imágenes directamente en el navegador al ejecutar el servidor local con python manage.py runserver.
Las modificaciones realizadas fortalecieron el proyecto al mejorar su funcionalidad, organización y seguridad. La creación de formularios personalizados permitió un manejo más claro del registro, inicio de sesión y publicación de artículos. Las nuevas vistas añadieron procesos esenciales como autenticar usuarios, mostrar detalles y agregar contenido, mientras que el uso de @login_required aseguró que ciertas acciones solo se realicen dentro de una sesión activa.
Además, las rutas actualizadas en urls.py facilitaron la navegación entre funciones, y las plantillas modificadas mejoraron la presentación y la experiencia del usuario. En conjunto, estos cambios hicieron la aplicación más completa, profesional y fácil de mantener.
```bash
