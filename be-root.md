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


