#Changer les DNS du Dump

## Pourquoi ?

Le dump epitech utilise le serveur DNS du bocal, sauf que ce serveur n'est pas toujours à jour.
Ainsi il est possible de se retrouver avec des sites ou des parties de sites qui ne fonctionnent pas.

Exemple: dans ma promo beaucoup on eu le problème des photos de profile "fantomes" sur facebook (i.e. elles ne s'affichaient pas)
Plus grave: chez moi, outlook ne s'ouvrait plus, thunderbird n'arrivaient pas non plus à s'y connecter.

## Comment résoudre ce problème ?

Si le serveur dns du bocal n'est pas à jour, alors il n'y a qu'a utiliser d'autres serveurs DNS
J'ai personnellement opté pour OpenDNS, mais vous pouvez très bien choisir n'importe quel serveurs que vous voulez (e.g. google)
Il suffira, au moment de mettre les ip, de changer pour le dns de votre choix

Prérequis: être sudo ou root sur Opensuse STD, si vous n'êtes pas root voir mon tuto (à venir).

```shell
sudo vim /etc/dhclient.conf
```

```vim
déplacer le cursor vers la fin du fichier
taper i

copier/coller ces 2 lignes

prepend domain-name-servers 208.67.222.222;
prepend domain-name-servers 208.67.220.220;

taper echap
taper ":x" et faire entrer
```

```shell
sudo reboot
```
