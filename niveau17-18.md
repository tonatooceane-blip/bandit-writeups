Bandit Niveau 17 → 18

Objectifs:

Comparez deux fichiers (passwords.old et passwords.new) avec diff pour trouver la ligne modifiée et obtenir le mot de passe du niveau 18.

Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit17
Mot de passe : [utiliser le mot de passe du niveau 16-17]
Fichiers cibles : passwords.old et passwords.new
Objectif : Trouver la ligne modifiée entre les deux fichiers

Approche:

Se connecter au niveau 17. Deux fichiers sont présents : passwords.old et passwords.new. Une seule ligne a été modifiée entre les deux. Utiliser diff pour comparer les fichiers et identifier la ligne qui a changé. Cette ligne contient le mot de passe du niveau 18.

Commandes:

-ssh bandit17@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 17.

-ls -la

Afficher les fichiers du répertoire.

Comparer les fichiers :

-diff mots de passe.anciens mots de passe.nouveaux

Afficher les différences entre les deux fichiers.

Ou :

-cat passwords.new | grep -v -f passwords.old

Afficher les lignes qui ne sont pas dans passwords.old.

La ligne affichée est le mot de passe du niveau 18.

Filtrer:

-sortie

Sortir de la session SSH.

Prochaine étape

ssh bandit18@bandit.labs.overthewire.org -p 2220