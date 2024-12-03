##Migraciones y Base de Datos
Después de definir un modelo, sincroniza la base de datos con estas instrucciones:

##Crear las migraciones:
```
python manage.py makemigrations
```
Esto genera un archivo de migración en la carpeta migrations.

##Aplicar las migraciones:
```
python manage.py migrate
```
Esto actualiza la base de datos con los cambios.

##Registrar el Modelo en el Administrador

Para administrar el modelo desde el panel de administración, regístralo en admin.py:
```
from django.contrib import admin
from .models import Producto

admin.site.register(Producto)
```
Visita el panel de administración en /admin para gestionar el modelo.