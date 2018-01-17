```
Attribut directorycommunebrand_set créé par foreignkey(quel type de relation ?)
```

```python
  def commune_brands(self):
      return self.directorycommunebrand_set.enabled()
      #equivalent
      return DirectoryCommuneBrand.objects.filter(directory_commune=self).enabled()
```
