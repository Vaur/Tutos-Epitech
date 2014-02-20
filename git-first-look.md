# Introduction à Git

## Présentation de Git

Git est un logiciel de gestion de version créer par Linus Torvalds, le créateur du kernel Linux.

Il permet de partager entre plusieurs personnes le code, mais également de revenir dans le temps. C'est-à-dire si vous modifiez un fichier déjà commit, vous pouvez toujours revenir à une version précédente.

Il y as beaucoup à dire sur Git aussi ce tutoriel sera découpé en plusieurs parties. Il existe déjà un [Cheat sheet](https://github.com/Vaur/Tutos-Epitech/blob/master/git-cheat-sheet.md) pour retrouver rapidement une commande git sans avoir à tout relire.

Cette première partie traitera principalement des bases de Git, pour partager et modifier du code facilement avec vos membres du groupes.

### Récupérer le dépôt

Quand le dépôt existe déjà (e.g. il a été créé par votre chef de groupe) on va le récupérer en faisant un git clone

```shell
<100%=~>git clone devill_x@git.epitech.eu:/devill_x/git_exemple
Cloning into 'git_exemple'...
remote: Counting objects: 2, done.
remote: Total 2 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (2/2), done.
Checking connectivity... done.
<100%=~>
```


