Bandit Niveau 13 → 14

Objectifs:

Utilisez une clé SSH privée pour se connecter au niveau 14 et lire le mot de passe.

Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit13
Mot de passe : [utiliser le mot de passe du niveau 12-13]
Fichier cible : Une clé SSH privée dans le répertoire home
Objectif : Se connecter à bandit14 avec la clé SSH

Approche:

Je me connecte avec le mot de passe du niveau 13. Un fichier de clé SSH privée est présent. Je l'utilise avec SSH pour me connecter directement au serveur bandit14, puis je lis le mot de passe dans /etc/bandit_pass/bandit14.

Commandes:

-ssh bandit13@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 13.

-ls -la

Afficher les fichiers. Rechercher une clé SSH privée.

-ssh -i [clé_privée] bandit14@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 14 avec la clé SSH privée.

Lire le mot de passe :

-cat /etc/bandit_pass/bandit14

Lire le mot de passe du niveau 14.

Extraire:

-sortie

Sortir de la session SSH.

Prochaine étape

ssh bandit14@bandit.labs.overthewire.org -p 2220