# Quelques problèmes avec les nombres décimaux


## Les nombres entiers

Un ordinateur est très fort pour calculer avec des nombres entiers.
Par exemple, aucun problème pour afficher 2**10000.

```python runnable
print("2**10000 =", 2**10000)
```

Même si ce nombre comporte 3011 chiffres…

```python runnable
longueur = len(str(2**10000))
print("Nombre de chiffres dans 2**10000 :", longueur)
```


## Les décimaux

En revanche, un ordinateur a quelques soucis avec les nombres décimaux : les flottants.

```python runnable
print("a =", 0.1)
print("b =", 0.2)
print("a + b =", 0.1+0.2)
```

Ce qui engendre quelques problèmes…

### Réciproque du théorème de Pythagore

Le triangle dont les côtés mesurent 1cm, 2,4cm et 2,6cm est rectangle.
C'est pas moi qui le dit, c'est le théorème de Pythagore :


```python runnable
a = 1
b = 2.4
c = 2.6
print("a**2 + b**2 =", a**2 + b**2)
print("c**2 =", c**2)
```

Ah non…

Et d'ailleurs, le test de la réciproque est bien faux (sic)

```python runnable
a = 1
b = 2.4
c = 2.6
print("a**2 + b**2 == c**2 : ", a**2 + b**2 == c**2)
```

