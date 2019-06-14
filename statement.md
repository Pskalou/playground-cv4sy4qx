# Quelques problèmes avec les nombres décimaux


## Les nombres entiers

Un ordinateur est très fort pour calculer avec des nombres entiers.
Par exemple, aucun problème pour afficher 2**10000.

```python runnable
print("2**10000 = ", 2**10000)
```

Même si ce nombre comporte 3011 chiffres…

```python runnable
longueur = len(str(2**10000))
print("Nombre de chiffres dans 2**10000 : ", longueur)
```


## Les décimaux

En revanche, un ordinateur a quelques soucis avec les nombres décimaux : les flottants.

```python runnable
print(0.1)
print(0.2)
print(0.1+0.2)
```
