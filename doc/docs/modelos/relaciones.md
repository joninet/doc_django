###Relación Uno a Muchos

```
class Categoria(models.Model):
    nombre = models.CharField(max_length=100)

class Producto(models.Model):
    nombre = models.CharField(max_length=100)
    categoria = models.ForeignKey(Categoria, on_delete=models.CASCADE)
```
`ForeignKey`: Crea una relación uno a muchos.

`on_delete=models.CASCADE`: Si se elimina la categoría, los productos asociados también se eliminan.

##Relación Muchos a Muchos
```
class Tienda(models.Model):
    nombre = models.CharField(max_length=100)

class Producto(models.Model):
    nombre = models.CharField(max_length=100)
    tiendas = models.ManyToManyField(Tienda)

```

##Relación Uno a Uno
```
class PerfilUsuario(models.Model):
    usuario = models.OneToOneField(User, on_delete=models.CASCADE)
    biografia = models.TextField(blank=True)
```


