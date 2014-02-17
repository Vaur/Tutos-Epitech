#Changer les DNS du Dump

## Pourquoi ?

Le dump Epitech utilise le serveur DNS du bocal, sauf que ce serveur n'est pas toujours à jour.
Ainsi il est possible de se retrouver avec des sites ou des parties de sites qui ne fonctionnent pas.

Exemple: dans ma promo beaucoup ont eu le problème des photos de profil "fantômes" sur Facebook (i.e. elles ne s'affichaient pas)
Plus grave: chez moi, outlook ne s'ouvrait plus, thunderbird n'arrivait pas non plus à s'y connecter.

## Comment résoudre ce problème ?

Si le serveur DNS du bocal n'est pas à jour, alors il n'y a qu'a utiliser d'autres serveurs DNS
J'ai personnellement opté pour les DNS de Google, mais vous pouvez très bien choisir n'importe quel serveur que vous voulez (e.g. OpenDNS)
Il suffira, au moment de mettre les IP, de changer pour le DNS de votre choix.

Prérequis: être sudo ou root sur Opensuse STD, si vous n'êtes pas root voir mon tuto (à venir).

```shell
sudo vim /
```

```
déplacer le cursor vers la ligne 281: 
taper i

changer la ligne suivante:
NETCONFIG_DNS_STATIC_SERVERS=""

et la remplacer par:
NETCONFIG_DNS_STATIC_SERVERS="8.8.8.8 8.8.4.4"

taper echap
taper ":x" et faire entrer
```

```shell
sudo reboot
```

