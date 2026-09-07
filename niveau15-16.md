Bandit Niveau 15 → 16

Objectifs:

Soumettre le mot de passe du niveau 15 au port 30001 sur localhost avec chiffrement SSL/TLS pour obtenir le mot de passe du niveau 16.

Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit15
Mot de passe : [utiliser le mot de passe du niveau 14-15]
Port cible : 30001 (localhost avec SSL/TLS)
Objectif : Soumettre le mot de passe du niveau 15 avec chiffrement SSL

Approche:

Se connecter au niveau 15. Lire le mot de passe dans /etc/bandit_pass/bandit15. Utilisez openssl s_client pour se connecter au port 30001 en SSL/TLS et soumettre le mot de passe.

Commandes:

-ssh bandit15@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 15.

-cat /etc/bandit_pass/bandit15

Lire le mot de passe du niveau 15.

Soumettre avec SSL/TLS :

-openssl s_client -connect localhost:30001

Connectez-vous au port 30001 avec chiffrement SSL/TLS.

Puis copier/coller le mot de passe du niveau 15.

Sélectionner

Sortir de la session SSH.

Prochaine étape:

ssh bandit16@bandit.labs.overthewire.org -p 2220