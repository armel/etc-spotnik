# Correctifs apportés sur le /etc/spotnik de la version 1.9.5

Principales évolutions:

- Fix des fichiers wav (merci AleX)
- Fix sur la gestion du timersalon parfois instable
- Clean du code

# A propos du fix sur la gestion du timersalon

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
- Le fait de lancer le script `timersalon.sh` en background permet de rendre la main et de revenir au menu de l'outil _spot_ CLI, lorsqu'il est utilisé pour changer de salon.

## Todo (à l'attention de F5NLG)

Non bloquant, mais penser à faire un `chown root:root` sur tous les fichiers du `/etc/spotnik`. Certains appartiennent à l'utilisateur et au group `jp` ;)

88 & 73 de F4HWN Armel.
