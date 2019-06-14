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

La réciproque du théorème de Pythagore fonctionne très bien avec les nombres **entiers**

```python runnable
a = 3
b = 4
c = 5
print(a**2 + b**2 == c**2)
```

Mais avec les nombres flottans, il peut y avoir quelques surprises…

```python runnable
a = 1
b = 2.4
c = 2.6
print(a**2 + b**2 == c**2)
```

En effet, les valeurs sont vraiments différentes et le test est donc faux… (domage)

```python runnable
a = 1
b = 2.4
c = 2.6
print(a**2 + b**2)
print(c**2)
```

