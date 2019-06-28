#Correctifs apportés sur le /etc/spotnik de la version 1.9.5

Principales évolutions:

- Fix des fichiers wav (merci AleX)
- Fix sur la gestion du timersalon parfois instable

#A propos du fix sur la gestion du timersalon

## Sur les fichiers restart.*

Modification des dernières lignes des fichiers `restart.*` [tec, int, loc, bav, fon, el]

```
# debut gestion timer salon:
pkill -f timersalon
sh /etc/spotnik/timersalon.sh &
```

## Sur le script timersalon.sh

Ajout du retour vers le salon RRF à la fin du script `timersalon.sh`

```
/etc/spotnik/restart.rrf
```

## Observations

- Semble corriger le bug de fonctionnement du timersalon parfois observé
- Le fait de lancer le script `timersalon.sh` en background permet de rendre la main et de revenir au menu `spot` lorsqu'il est utilisé pour changer de salon.

88 & 73 de F4HWN Armel.
