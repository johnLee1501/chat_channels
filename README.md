# ChatDjango

Este proyecto contiene un chat básico donde puedes crear una sala y comunicarte con todas las personas que entren a la misma sala.

### Algunas características principales: 




## Getting Started

Estas instrucciones te proporcionarán una copia del proyecto en funcionamiento en tu máquina local con fines de desarrollo y prueba.

### Prerrequisito

Si quieres probar, necesitarás estos requisitos previos

```
Python > 3.6
```

### Instalación

Primero, clona el proyecto en tu computadora

```
git clone https://github.com/johnLee1501/chat_channels.git
```

luego, cree un entorno virtual para el proyecto, puede usar virtualenvwrapper-win si su sistema operativo es Windows

```
pip install virtualenvwrapper-win
mkvirtualenv <nombre_del_entorno>
```

después de eso, instala los paquetes en requirements.txt para asegurarte de tener todo lo necesario

```
pip install -r requirements.txt
```}

por último realiza las migraciones de tu modelo a la base de datos.
```
py manage.py makemigrations
py manage.py migrate
```

Listo! ya puedes ejecutarlo

```
py manage.py runserver
```


## Autor

* **John Vega**

## Screenshots
