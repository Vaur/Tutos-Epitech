# Gitignore : forcer git à ignorer des fichiers

## Explications

Il arrive lorsque l'on travaille sur un projet que les membres de son groupe se mettent à envoyer sur le dépôt des fichiers qui n'ont strictement rien à y faire. Exemple: les .o et les binaires générés par le Makefile.

Ce genre de choses alourdissent énormément le dépot. Ainsi dans l'un de mes projets, les extensions .o représentaient 78.81% du dépôt total.

Pour éviter de retrouver son dépôt avec des fichiers absolument inutiles il suffit de créer un fichier .gitignore à la racine de son dépôt qui contiendra les fichiers à ignorer et de le commit.

Exemple:

```.gitignore
bomberman ## le binaire qui est généré par le makefile

*.o ## les fichiers temporaires créés par le makefile

*.~ ## les sauvegardes créés lorsqu'on a édité un fichier

```

Vous pouvez également trouver mon .gitignore ici: [gitignore](https://github.com/Vaur/Tutos-Epitech/blob/master/.gitignore)
