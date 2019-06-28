/etc/spotnik fix

- Fix des fichiers wav (merci AleX)
- Fix sur la gestion du timersalon parfois instable

--> modification des dernières lignes des fichiers restart.* [tec, int, loc, bav, fon, el]

# debut gestion timer salon:
pkill -f timersalon
sh /etc/spotnik/timersalon.sh &

--> ajout du retour vers le salon RRF à la fin du script timersalon.sh

/etc/spotnik/restart.rrf

Observation:
- semble corriger le bug de fonctionnement du timersalon parfois observé
- le fait de lancer le script timersalon.sh en background permet de rendre la main et de revenir au menu spot

88 & 73 de F4HWN Armel.
