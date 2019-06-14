# Quelques problèmes avec les nombres décimaux

Python est très fort pour calculer avec des nombres entiers.
Par exemple, aucun problème pour afficher 2**10000.

```python runnable
print("2**10000 = ", 2**10000)
```

Même si ce nombre comporte 3011 chiffres…

```python runnable
longueur = len(str(2**10000))
print("Longueur de $2^10000$", longueur)
```
