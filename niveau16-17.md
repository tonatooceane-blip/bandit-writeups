Bandit Niveau 16 → 17

Objectifs:

Scanner les ports 31000-32000 sur localhost pour trouver un serveur qui renvoie une clé SSH privée.

Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit16
Mot de passe : [utiliser le mot de passe du niveau 15-16]
Plage de ports : 31000-32000 (localhost)
Objectif : Trouver la clé SSH privée parmi les serveurs

Approche:

Se connecter au niveau 16. Scanner les ports 31000-32000 sur localhost avec nmap pour identifier les ports ouverts. Connectez-vous à chaque port avec openssl s_client ou nc et soumettez le mot de passe. Un seul serveur renverra la clé SSH privée.

Commandes:

-ssh bandit16@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 16.

-nmap -p 31000-32000 localhost

Scanner les ports 31000-32000 pour trouver les serveurs actifs.

Identifier le bon port :

-openssl s_client -connect localhost:[port]

Connectez-vous à un port avec SSL/TLS.

Soumettre le mot de passe du niveau 16.

Ou :

-nc localhost [port]

Utilisez netcat pour vous connecter.

Répétez pour chaque port jusqu'à trouver la clé SSH privée.

Filtrer:

-sortie

Sortir de la session SSH.

Prochaine étape

Utilisez la clé SSH privée pour se connecter au niveau 17.