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
a = 0.1
b = 0.2
print(a+b)
```

Ce qui engendre quelques problèmes…

### Réciproque du théorème de Pythagore


#### Le problème

La réciproque du théorème de Pythagore fonctionne très bien avec les nombres **entiers**

```python runnable
# Premier triangle rectangle
a = 3
b = 4
c = 5
print(a**2 + b**2 == c**2)
```

Mais avec les nombres flottans, il peut y avoir quelques surprises…

```python runnable
# Premier triangle rectangle
a = 3
b = 4
c = 5
print(a**2 + b**2 == c**2)

# Deuxième triangle rectangle
a = 1
b = 2.4
c = 2.6
print(a**2 + b**2 == c**2)

# Troisième triangle rectangle
a = 20.8
b = 30.6
c = 37
print(a**2 + b**2 == c**2)
```

En effet, les valeurs sont vraiments différentes et le test est donc faux… (domage)

```python runnable
# Premier triangle rectangle
a = 3
b = 4
c = 5
print(a**2 + b**2)
print(c**2)

# Deuxième triangle rectangle
a = 1
b = 2.4
c = 2.6
print(a**2 + b**2)
print(c**2)

# Troisième triangle rectangle
a = 20.8
b = 30.6
c = 37
print(a**2 + b**2)
print(c**2)

```

#### Une solution possible

Une solution est de remplacer **le test d'égalité entre flottant** par une **un test d'inégalité**.


```python runnable
# Premier triangle rectangle
a = 3
b = 4
c = 5
print( abs(a**2 + b**2 - c**2) < 1e-10 )

# Deuxième triangle rectangle
a = 1
b = 2.4
c = 2.6
print( abs(a**2 + b**2 - c**2) < 1e-10 )

# Troisième triangle rectangle
a = 20.8
b = 30.6
c = 37
print( abs(a**2 + b**2 - c**2) < 1e-10 )
```

Une autre solution consiste à **arrondir** les nombres flottant.


```python runnable
# Premier triangle rectangle
a = 3
b = 4
c = 5
print( round(a**2 + b**2,10) == round(c**2,10) )

# Deuxième triangle rectangle
a = 1
b = 2.4
c = 2.6
print( round(a**2 + b**2,10) == round(c**2,10) )

# Troisième triangle rectangle
a = 20.8
b = 30.6
c = 37
print( round(a**2 + b**2,10) == round(c**2,10) )
```

