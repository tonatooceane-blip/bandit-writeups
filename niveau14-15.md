Bandit Niveau 14 → 15

Objectifs:

Soumettre le mot de passe du niveau 14 au port 30000 sur localhost pour obtenir le mot de passe du niveau 15.

Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit14
Mot de passe : [utiliser le mot de passe du niveau 13-14]
Port cible : 30000 (localhost)
Objectif : Soumettre le mot de passe du niveau 14 pour obtenir celui du niveau 15

Approche:

Se connecter au niveau 14. Lire le mot de passe dans /etc/bandit_pass/bandit14. Soumettre ce mot de passe au port 30000 sur localhost en utilisant telnet ou nc.

Commandes:

-ssh bandit14@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 14.

-cat /etc/bandit_pass/bandit14

Lire le mot de passe du niveau 14.

Soumettre le mot de passe :

-telnet localhost 30000

Soumettre le mot de passe au port 30000 en utilisant telnet.

Ou :

-nc localhost 30000

Utilisez netcat pour soumettre.

Puis copier/coller le mot de passe du niveau 14.

Isoler:

-sortie

Sortir de la session SSH.

Prochaine étape

ssh bandit15@bandit.labs.overthewire.org -p 2220