# Gitignore : forcer git a ignorer des fichiers

## Explications

Il arrive lorsque l'on travail sur un projet que les membres de son groupe se mette à envoyer sur le dépot des fichiers qui n'ont strictement rien à faire sur le dépots. Exemple: les .o et les binaires généré par le makefile.

Ce genre de chose alourdi énormément le dépot. Ainsi dans l'un de mes projets. Les points .o représentait 78.81% du dépot total.

Pour éviter de retrouver son dépot avec des fichiers absolument inutile. Il suffit de créer un fichier .gitignore à la racine de son dépot, qui contient les fichiers à ignorer et de le commit.

Exemple:

```.gitignore
bomberman ## le binaire qui est généré par le makefile

*.o ## les fichiers temporaires créer par le makefile

*.~ ## les sauvegardes créé lorsqu'on a édité un fichier

```

Vous pouvez également trouver mon .gitignore ici: [gitignore](https://github.com/Vaur/Tutos-Epitech/blob/master/.gitignore)
