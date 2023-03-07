
### Programme 1 : Affichage

Laquelle des quatres instructions Python suivantes permet d'afficher en console : `Bonjour`

- `ecrit("Bonjour")`
- `affiche("Bonjour")`
- `print("Bonjour")`
- `print("Hello")`


### Programme 2 : Concaténation

La séquence d'instructions Python :

```python
mot = 'Bonjour'
votre_nom = 'Toto'
print(mot + votre_nom)
```
produit en console l'affichage : `BonjourToto`

- Modifier la troisième instruction pour obtenir l'affichage : `Bonjour Toto` ;
- Proposer une autre solution pour obtenir l'affichage : `Bonjour Toto` mais sans modifier la troisième instruction.


### Programme 3 : Boucle

Combien de fois l'instruction Python `action()` est-elle effectuée dans chaque cas ?

- Cas n°1
```python
for tour in range(10) :
    action()
```

- Cas n°2
```python
init()
action()
for tour in range(12) :
    action()
    inter()
    action()
fin()
action()
```

- Cas n°3
```python
for tour_1 in range(10):
    for tour_2 in range(5):
        action()        
```

- Cas n°4
```python
for tour_1 in range(10):
    action()
    for tour_2 in range(5):
        action()
        post()
action()
```


### Programme 4 : Test de condition

Le tarif d’un musée est le suivant :
- Adulte (plus de 18 ans) : 17€ ;
- Enfant de plus de 9 ans : 10€ ;
- Enfant de 9 ans ou moins : 4€.

Compléter le programme Python suivant qui demande l'âge d'un visiteur et affiche le prix à payer :

```python
age = int(input("Quel est votre âge ?"))

if age <= 9 : 

    prix = ..............

elif ............................ :
    
    prix = ..............

else :

    prix = 10

print("Prix à payer : " , prix, "euros")
```


D’une manière générale, en algorithmique, que sont age et prix dans le programme 4, ou encore mot et votre_nom dans le programme 2 ?

