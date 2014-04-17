# Git Cheatsheet

Liste de commandes qui peuvent servir pour utiliser les dépots Git fourni par Epitech:

## Git basic

Ajouter un fichier sous revision

```git
git add fichier
```

Enregistrer les changements

```git
git commit -m "message de commit"
```

Envoyer les changements au serveur

```git
git push
```

Récupérer les modifications depuis le serveur (à faire de préfèrence avant de push)

```git
git pull
```

Se connecter à un dépot déjà existant (remplacer depot par le nom du dépôt, login par votre login et login_prop par le login du propriétaire du dépot)

```git
git clone login@git.epitech.eu:/login_prop/depot
```

Ajouter un dépot remote à un dépot local déjà existant:

```git
git remote add origin login@git.epitech.eu:/login_prop/depot
git push origin master
```

## Gestion du dépot Epitech avec BLIH

Créer un dépot de rendu

```blih
blih repository create nom_du_depot
```

Donner les accès au dépot (remplacer login par le login de la personne pour qui vous voulez donner les droits).
Les droits d'accès existant sont: r (lecture seul), w (écriture seul) et rw (lecture et écriture).
Attention, si vous donnez uniquement w la personne ne pourra pas clone le dépot, ni récupérer les changements.

```blih
blih repository setacl nom_du_depot login rw
```

Voir les droits d'accès du dépots:

```blih
blih repository getacl test
```

## Gestion de plsuieurs repos

Je possède un serveur privé sur le quel j'envois mes commits en plus du dépot d'epitech.
Voici quelques commandes pour gérer un tel cas.

Ajouter un serveur remote
```git
git remote add nom_remote user@url_remote
```

Envois d'une branch à remote
```git
git push -u nom_remote branch
```

Créer un repertoire sur remote (pour pouvoir lui envoyer ce que vous avez déjà fait)
```bash
mkdir repository && cd repository
git init --bare
```
Ajouter une branch provenant d'un remote.

```git
git fetch remote branch_remote:branch_local
```

# Plus ?

Si vous voulez un vrai tuto sur git, n'hésitez pas à m'envoyer un [email](mailto:xavier.devilliers@epitech.eu). Git étant un outil très puissant, il y a beaucoup à couvrir.
