# ChatDjango

Este proyecto contiene un chat básico donde puedes crear una sala y comunicarte con todas las personas que entren a la misma sala.

### Algunas características principales: 
- Creación de multiples salas
- Almacenamiento de mensajes asociados a salas y usuarios
- Chat Consumer asíncrono

### Guía Rápida

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

Luego, crea un entorno virtual para el proyecto, puedes usar virtualenvwrapper-win si su sistema operativo es Windows

```
pip install virtualenvwrapper-win
mkvirtualenv <nombre_del_entorno>
```

Después de eso, instala los paquetes en requirements.txt para asegurarte de tener todo lo necesario

```
pip install -r requirements.txt
```

Realiza las migraciones de tu modelo a la base de datos.
```
py manage.py makemigrations
py manage.py migrate
```
Iniciar un servidor Redis en el puerto 6379 (Necesitas tener instalado docker desktop en tu máquina). Ejecuta el siguiente comando:
```
docker run -p 6379:6379 -d redis:5
```
Si no deseas instalar redis y prefieres optar por una solución más sencillá, puedes utilizar un canal de testing:
Ve a settings.py y remplaza la configuración del canal:
```
CHANNEL_LAYERS = {
    'default': {
        'BACKEND': 'channels_redis.core.RedisChannelLayer',
        'CONFIG': {
            "hosts": [os.environ.get('REDIS_URL', 'redis://localhost:6379')],
        },
    },
}
```
por esto
```
CHANNEL_LAYERS = {
    "default": {
        "BACKEND": "channels.layers.InMemoryChannelLayer"
    }
}
```
Listo! ya puedes ejecutarlo

```
py manage.py runserver
```


## Autor

* **John Vega**

## Screenshots

![image](https://user-images.githubusercontent.com/71096926/121255053-94024080-c870-11eb-93db-d3ba2ce203b9.png)

![image](https://user-images.githubusercontent.com/71096926/121255273-d461be80-c870-11eb-87ce-b79ec0142aed.png)

