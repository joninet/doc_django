# Modelos en Django

Los modelos representan las tablas y su estructura en la base de datos. En Django, cada modelo es una clase que hereda de `django.db.models.Model`.

---

## Crear un Modelo Básico

Define los modelos en el archivo `models.py` de tu aplicación:

```python
from django.db import models

class Producto(models.Model):
    nombre = models.CharField(max_length=100)  # Campo de texto
    precio = models.DecimalField(max_digits=10, decimal_places=2)  # Número decimal
    fecha_creacion = models.DateTimeField(auto_now_add=True)  # Fecha automática al crear

    def __str__(self):
        return self.nombre
```
## Campos Comunes en Modelos

`CharField`: Almacena texto, con una longitud máxima.

`DecimalField`: Almacena números decimales.

`DateTimeField`: Almacena fechas y horas. Usa auto_now_add para registrar automáticamente la fecha al crear el registro.

