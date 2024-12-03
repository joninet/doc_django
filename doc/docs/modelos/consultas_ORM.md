##Consultas Básicas con el ORM
Interacciona con los modelos usando el ORM (Object-Relational Mapper):

##Crear registros:

```
Producto.objects.create(nombre="Celular", precio=1200.50)
```
##Obtener todos los registros:

```
productos = Producto.objects.all()
```
##Filtrar registros:

```
productos_baratos = Producto.objects.filter(precio__lt=500)  # Menores a $500
```
##Actualizar registros:

```
producto = Producto.objects.get(id=1)
producto.precio = 1500.00
producto.save()
```
##Eliminar registros:

```
producto = Producto.objects.get(id=1)
producto.delete()
```