#Etre Root

##Pourquoi ?

Il y a plusieurs avantages au fait d'être root sur le dump. Tout d'abord vous pourrez appliquer d'autres tutos présent sur le dépot 
(i.e. [Changer les DNS](https://github.com/Vaur/Tutos-Epitech/blob/master/change-dns.md#changer-les-dns-du-dum).
Installer d'autres programmes, ou encore avoir un total contrôle sur votre dump. 


## Avertissement

> Un grand pouvoir implique une grande responsabilité
Voltaire

Attention, une fois root, vous pouvez faire tout et n'importe quoi sur vos dump. Si vous faites une connerie vous êtes le seul responsable, surtout si vous devez redump.

Si je n'ai pas effrayé tout le monde avec mon avertissement, on va pouvoir passer à la suite.

## Booter le dump en single user

On va tout d'abord booter sur Opensuse STD en mode single user. Au moment où vous êtes sur le GRUB:

```
selectionner Opensuse STD
taper e



entrer
```

Vous êtes maintenant en mode single user. Avant de passer root ou sudo il faut se mettre en azerty.

```shell
loadkeys fr
```

##Passer Root

Pour être root sur votre machine c'est très simple:

```shell
passwd
```

Taper 2 fois le mot de passe de votre choix, puis entrer.
En cas de Warning tel que:

```passwd
BAD PASSWORD: it is based on a dictionary word
BAD PASSWORD: is too simple
```

Ne pas s'alarmer, surtout ne pas changer de mot de passe. Mettez bien le même mot de passe, que vous avez entré la première fois. Il peut vous arriver des surprises

##Passer sudo

Passer sudo est à peine plus compliqué que ça.
Tout d'abord:

```shell
sudo vim /etc/sudoers
```

```
se déplacer ligne 61

taper i


ajouter ## devant ces deux lignes:

Defaults targetpw   # ask for the password of the target user i.e. root
ALL   ALL=(ALL) ALL   # WARNING! Only use this together with 'Defaults targetpw'!

Vous devriez maintenant avoir:

##Defaults targetpw   # ask for the password of the target user i.e. root
##ALL   ALL=(ALL) ALL   # WARNING! Only use this together with 'Defaults targetpw'!

descendre jusqu'à la ligne 72
en dessous de la ligne : "root ALL=(ALL) ALL" 

ajouter la ligne:
votre_login ALL=(ALL) ALL

faire echap
taper
:x
faire entrer
```

Pour quitter le mode single user appuyer sur le boutton de démarrage jusqu'à ce que votre ordi s'éteigne.
