# Python pour le Cevipof

_Mercredi 7 octobre 2020 par visioconférence_

## Généralités sur Python

Python est un langage interprété. Pas de compilateur. L'interpréteur pour Python 3.6 (3.7 ?) est installé par défaut sur Windows 10 et Mac OS 10.??. Mais aussi sous Android, iOS.

C'est un langage de programmation orienté objet. On peut y créer des objet ayant des fonctions et des attributs. Pensez à une caisse enregistreuse de supermarché, c'est un objet, avec ses fonctions, ses entrées, ses sorties.

C'est un langage avec un typage dynamique. Une variable manipulée peut changer de type et rechanger de type. Elle en a néanmoins un : entier, décimal, chaîne de caractères, booléen ou rien (None).

Python est doté d'un garbage collector (gestion de l'attribution d'espace mémoire automatisé) et d'un système de gestion d'exception. C'est un langage de haut niveau : sa syntaxe est simple (comparée à java ou C).

Python est sous licence libre.

« Il faut treize paragraphes pour expliquer un Hello, World! en C++, seulement deux en Python »

~~~ Python
print("Hello, world!!!")
~~~

C'est un langage [polyvalent](https://www.jetbrains.com/lp/devecosystem-2019/python/) et [populaire](http://pypl.github.io/PYPL.html). De nombreuses enquêtes d'usage le donne comme grand gagnant ces dernières années, c'est probablement la raison pour laquelle ce cours a lieu.

## Remarques sur la syntaxe du Python

### Lisibilité

Python a été conçu pour être un langage lisible. Un bout de code est donc visuellement épuré.

~~~ Python
def absolute_value(num):
    # This function returns the absolute value of the entered number

    if num >= 0:
        return num
    else:
        return -num

print(absolute_value(2))
print(absolute_value(-4))
~~~

### Indentation et retours chariot

L'indentation est sémantique. Les blocs de codes (conditions, boucles, fonctions, classes, etc...) sont définis par l'indentation, et pas des accolades comme ça peut l'être couramment (C, C++, Java, etc...).

~~~ Python
x = 4

if x = 4:
    x = x + 1

print(x)
~~~

Les retours chariot le sont donc aussi : pas de marque de fin de ligne ou d'instruction nécessaire : Java a besoin d'un ; à chaque fin d'instruction

### Parenthèses

Pas de parenthèses pour les conditions comme le _if_ ci-dessus, mais elles sont évidemment importantes et nécessaires pour la priorité des opérations, mathématiques et logiques.

Les parenthèses sont utilisées dans la définition et l'appel des fonctions pour en préciser les arguments

~~~ Python
def mafonction(monparam)
    monparam = monparam + 1
    return monparam

x = 4

if x = 4:
    x = mafonction(x)

print(x)

~~~

Les crochets et les accolades ont aussi une place dans la syntaxe, ne vous inquiétez pas.

#### Mots-clés

Les mots-clés sont en nombre fini et réduit : 30

- and
- as
- assert
- break
- class
- continue
- def
- del
- elif
- else
- except
- exec
- finally
- for
- from
- global
- if
- import
- in
- is
- lambda
- not
- or
- pass
- print
- raise
- return
- try
- while
- with
- yield

### Avancé

La Python Software Foundation responsable de Python publie le [Python Enhancement Proposals](https://www.python.org/dev/peps/pep-0008/). Il contient un guide de "style" pour la programmation en Python. Pour ceux qui tiennent à produire du BEAU code.

## Wrap-up

Tout ça pour dire que c'est un langage épuré, syntaxiquement simple, donc facile à aborder et qui est largement utilisé.

## Ressources de formation

### Cours en ligne

- [Learn Python](https://www.learnpython.org/en/Hello%2C_World%21) : le mooc officiel python. Un cours bien construit qui manque un peu d'exercices au départ à mon gout...
- [Codecademy](https://www.codecademy.com/learn/learn-python) : un cours construit uniquement autour d'exercices. Pas assez d'explication à mon goût lorsqu'on atteint les niveaux les plus avancés.
- Les exemples très utiles de la [W3School](https://www.w3schools.com/python/python_examples.asp)
- [Sur Udemy](https://www.udemy.com/course/pythonforbeginnersintro), [de nombreux cours gratuits](https://www.udemy.com/course/learn-python-3-from-scratch-python-for-absolute-beginners)

### Documentation

- [Stack Overflow](https://stackoverflow.com/questions/tagged/python) : LE site qui répondra à toutes vos questions techniques de code. Tapez une question de programmation dans google, ce sera la première réponse.
- [Documentation Python](https://docs.python.org/3) : la documentation officielle du langage python. Elle est moche, mais c'est ici que vous trouverez le descriptif des fonctions du langage. Exemple : la fonction [print()](https://docs.python.org/3/library/functions.html#print)
- [Google](https://www.lmgtfy.com) : moteur de recherche très performant. Formulez vos problèmes de Python en anglais permet d'obtenir plus de résultats.

## Installation de l'environnement de travail

Il y a de nombreuses manières de coder en python :

- Un [éditeur de texte](https://atom.io/) comme Atom + un terminal sur sa machine
- Un [Integrated Development Environment](http://www.jetbrains.com/pycharm/) ou IDE, tout-en-un
- Un [environnement de programmation en ligne](https://repl.it/), un IDE en ligne, limité mais pratique
- Des [Jupyter Notebooks](http://jupyter.org/), adapté l'apprentissage en groupe et à l'utilisation en sciences

### Google Colaboratory

Nous avons accès à la solution d'hébergement de Jupyter Notebook de Google grâce à notre adresse @sciencespo.fr : [Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb) (pour colaboratory).

__Pour l'utiliser :__
- Connectez-vous à votre drive avec votre adresse @sciencespo.fr
- Créez un dossier dans lequel vous stockerez tous les documents relatifs à ce cours
- En faisant un clic-droit dans le dossier, puis "Plus" en fin de liste : soit Colaboratory est déjà une option, soit il vous faudra "Connecter plus d'applications..."
- Installer Google Colaboratory en le cherchant dans les applications disponibles, si nécessaire
- (Il est souvent nécessaire de se déconnecter puis se reconnecter à son compte Google pour rendre l'installation effective)
- Créer alors un nouveau document Colaboratory dans votre dossier drive : Nouveau > Plus > Colaboratory
- Vous vous retrouvez dans un Google Doc un peu particulier : un _Notebook Jupyter_.

Un notebook fonctionne par _cellules_ dans lesquelles on peut écrire du texte ou du code Python. La première cellule du document est une cellule de code, libre à vous de créer des cellules avec les boutons CODE et TEXT disponibles.

Lorsque vous écrivez du code dans une cellule, le bouton Play sur la gauche de la cellule permet d'executer ce code. Le résultat apparaît immédiatement au-dessous de la cellule.

### Installation locale

Je n'ai jamais fait ça sur Windows mais ça paraît très simple dans [ce tutoriel](https://docs.python-guide.org/starting/install3/win/#install3-windows).

Le workflow devient alors :

- Coder dans un éditeur de texte adapté ([Atom](https://atom.io/))
- Sauvegarder son code dans un fichier avec une extension _.py_
- Utiliser son invite de commande ou son terminal pour naviguer jusqu'au dossier contenant le fichier.py
- Lancer son code en utilisant la commande _python fichier.py_
- Interpréter les erreurs que l'invite de commande renvoie
- Recommencer

## Mon cours de Python pour débutant

Mon cours est stocké dans des jupyter notebook dans mon drive.

Sous réserve d'accès, le cours commence [ici](https://colab.research.google.com/drive/1RIEUnetz-N8WrFhEM-gR-MxOYQOFnq4b#scrollTo=geokcC5vAEsI).

Il couvre les bases du langage en 3 documents. Le cours [2](https://colab.research.google.com/drive/1jbQ5AKySus4fimb-Q3A6vHdyUOwGcpAQ) et [3](https://colab.research.google.com/drive/18bzYOBLl6XL3otS89avzei03lxT0HU1I).

Mais n'importe quel tutoriel fera la même chose.

## Organisation du travail

- Comment avancer entre les séances ?
- Quels objectifs se donner ?
- Quel projet doit nous animer semaine après semaine ?

## Github

Github est une plateforme d'hébergement et de partage de code en ligne.
