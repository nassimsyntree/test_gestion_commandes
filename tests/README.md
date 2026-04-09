# 50 Commandes Python Essentielles

## 1. Types et variables

```python
# 1. Afficher dans la console
print("Hello, World!")

# 2. Déclarer une variable
nom = "Alice"

# 3. Connaître le type d'une variable
type(nom)  # <class 'str'>

# 4. Convertir en entier
int("42")  # 42

# 5. Convertir en string
str(100)  # "100"

# 6. Convertir en float
float("3.14")  # 3.14
```

## 2. Chaînes de caractères

```python
# 7. Longueur d'une chaîne
len("Python")  # 6

# 8. Mettre en majuscules
"hello".upper()  # "HELLO"

# 9. Mettre en minuscules
"HELLO".lower()  # "hello"

# 10. Remplacer dans une chaîne
"hello world".replace("world", "Python")  # "hello Python"

# 11. Découper une chaîne
"a,b,c".split(",")  # ["a", "b", "c"]

# 12. Joindre une liste en chaîne
",".join(["a", "b", "c"])  # "a,b,c"

# 13. Supprimer les espaces
"  hello  ".strip()  # "hello"

# 14. F-string (formatage)
age = 25
f"J'ai {age} ans"
```

## 3. Listes

```python
# 15. Créer une liste
fruits = ["pomme", "banane", "cerise"]

# 16. Ajouter un élément
fruits.append("orange")

# 17. Supprimer un élément
fruits.remove("banane")

# 18. Trier une liste
fruits.sort()

# 19. Inverser une liste
fruits.reverse()

# 20. List comprehension
carres = [x**2 for x in range(10)]

# 21. Filtrer avec list comprehension
pairs = [x for x in range(20) if x % 2 == 0]

# 22. Accéder à une tranche (slice)
fruits[1:3]
```

## 4. Dictionnaires

```python
# 23. Créer un dictionnaire
personne = {"nom": "Alice", "age": 30}

# 24. Accéder à une valeur
personne["nom"]  # "Alice"

# 25. Accéder avec valeur par défaut
personne.get("email", "inconnu")

# 26. Ajouter / modifier une clé
personne["ville"] = "Paris"

# 27. Lister les clés
personne.keys()

# 28. Lister les valeurs
personne.values()

# 29. Itérer sur un dictionnaire
for cle, valeur in personne.items():
    print(cle, valeur)
```

## 5. Fichiers

```python
# 30. Lire un fichier
with open("fichier.txt", "r") as f:
    contenu = f.read()

# 31. Écrire dans un fichier
with open("fichier.txt", "w") as f:
    f.write("Hello")

# 32. Lire ligne par ligne
with open("fichier.txt") as f:
    for ligne in f:
        print(ligne.strip())
```

## 6. Fonctions et contrôle de flux

```python
# 33. Définir une fonction
def saluer(nom):
    return f"Bonjour {nom}"

# 34. Fonction lambda
carre = lambda x: x**2

# 35. Condition if/elif/else
if x > 0:
    print("positif")
elif x == 0:
    print("zéro")
else:
    print("négatif")

# 36. Boucle for
for i in range(5):
    print(i)

# 37. Boucle while
while x > 0:
    x -= 1

# 38. Try / except
try:
    resultat = 10 / 0
except ZeroDivisionError:
    print("Division par zéro")
```

## 7. Modules et imports

```python
# 39. Importer un module
import os

# 40. Lister les fichiers d'un dossier
os.listdir(".")

# 41. Vérifier si un fichier existe
os.path.exists("fichier.txt")

# 42. Importer datetime
from datetime import datetime
maintenant = datetime.now()

# 43. Importer json
import json
data = json.loads('{"a": 1}')
json.dumps(data)
```

## 8. Fonctions utilitaires built-in

```python
# 44. Map — appliquer une fonction à chaque élément
list(map(str.upper, ["a", "b", "c"]))

# 45. Filter — filtrer les éléments
list(filter(lambda x: x > 0, [-1, 0, 3, -5, 8]))

# 46. Zip — combiner deux listes
list(zip(["a", "b"], [1, 2]))  # [("a", 1), ("b", 2)]

# 47. Enumerate — itérer avec index
for i, val in enumerate(["a", "b", "c"]):
    print(i, val)

# 48. Sorted avec clé custom
sorted(["banane", "ab", "cerise"], key=len)

# 49. Any / All
any([False, True, False])  # True
all([True, True, False])   # False

# 50. Input utilisateur
reponse = input("Ton nom ? ")
```
