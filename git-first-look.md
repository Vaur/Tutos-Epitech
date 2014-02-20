# Introduction à Git

## Présentation de Git

Git est un logiciel de gestion de version créer par Linus Torvalds, le créateur du kernel Linux.

Il permet de partager entre plusieurs personnes le code, mais également de revenir dans le temps. C'est-à-dire si vous modifiez un fichier déjà commit, vous pouvez toujours revenir à une version précédente.

Il y as beaucoup à dire sur Git aussi ce tutoriel sera découpé en plusieurs parties. Il existe déjà un [Cheat sheet](https://github.com/Vaur/Tutos-Epitech/blob/master/git-cheat-sheet.md) pour retrouver rapidement une commande git sans avoir à tout relire.

Cette première partie traitera principalement des bases de Git, pour partager et modifier du code facilement avec vos membres du groupes.

### Récupérer le dépôt

Quand le dépôt existe déjà (e.g. il a été créé par votre chef de groupe) on va le récupérer en faisant un git clone

```shell
  <99%-~/epitech/tutos>git clone devill_x@git.epitech.eu:/devill_x/git_exemple
  Cloning into 'git_exemple'...
  remote: Counting objects: 2, done.
  remote: Total 2 (delta 0), reused 0 (delta 0)
  Receiving objects: 100% (2/2), done.
  Checking connectivity... done.
  <99%-~/epitech/tutos>ls
  git_exemple
  <98%-~/epitech/tutos>ls git_exemple/
  <98%-~/epitech/tutos>
```

Que s'est-il passé ? Git s'est connecté au serveur git d'epitech (git.epitech.eu) et a récupérer une copie de devill_x/git_exemple. Il en a créer une copie locale du dépots qui ne contient rien. On va donc rajouter des fichiers.

```shell

<88%-~/epitech/tutos/git_exemple>echo "coucou" > test
<87%-~/epitech/tutos/git_exemple>echo "coucou" > test2
<87%-~/epitech/tutos/git_exemple>ls
test  test2
```

Nos fichiers sont maintenant créé. Voyons ce que Git a à dire à propos de notre dépot.

```shell
<86%-~/epitech/tutos/git_exemple>git status
On branch master
Your branch is up-to-date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

          test
          test2

nothing added to commit but untracked files present (use "git add" to track)
<85%-~/epitech/tutos/git_exemple>
```

La première ligne indique que l'on est sur la branch "master". Elle ne sert uniquement si vous utilisiez les branch, je reviendrais plus tard sur cette notion. La seconde ligne nous indique que notre branch "master" est à jour avec "origin/master", c'est-à-dire que votre branch n'a pas de modifications qui sont enregistrer qui n'ont pas été envoyer au serveur (appellé origin).

La ligne suivante nous indique les fichiers qui ne sont pas suivis par Git. On y retrouve nos deux fichiers. Git n'enregistre les modifications des fichiers que sur ceux qui sont "sous surveillance". On va donc lui demander de suivre l'état de ces fichiers. 

```shell
<74%-~/epitech/tutos/git_exemple>git add test test2
<74%-~/epitech/tutos/git_exemple>git status
On branch master
Your branch is up-to-date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

          new file:   test
          new file:   test2

<74%-~/epitech/tutos/git_exemple>
```

On viens donc d'ajouter nos fichiers à la liste de Git, maintenant il faut enregistrer les changements, on va "commit".

```shell
<74%-~/epitech/tutos/git_exemple>git commit -m "Ajout de test et test2"
[master 621a3b5] Ajout de test et test2
 2 files changed, 2 insertions(+)
   create mode 100644 test
   create mode 100644 test2
<63%-~/epitech/tutos/git_exemple>git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working directory clean
```

Git nous informe que notre répertoire de travail est propre, il n'y a rien à commit et il n'y as pas non plus de fichiers que Git ne connaitrais pas. Cependant, notre branch master est en avance par rapport à la branch master d'origin.
C'est-à-dire que nos modifications sont bien enregistré en local, mais elles ne sont pas présente sur le serveur.




