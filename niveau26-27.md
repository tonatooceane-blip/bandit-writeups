Bandit Niveau 26 → 27

Objectifs:

Utilisez le shell alternatif du niveau 26 pour récupérer le mot de passe du niveau 27.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit26
Mot de passe : [utiliser le mot de passe du niveau 25-26]
Cible : Accéder au mot de passe avec le shell alternatif

Objectif : Récupérer le mot de passe du niveau 27

Approche:

Se connecter au niveau 26 avec le shell alternatif découvert au niveau précédent. Utilisez les commandes disponibles dans ce shell pour explorer le répertoire home et récupérer le mot de passe du niveau 27.

Commandes:

-ssh bandit26@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 26.

Explorer le répertoire :

-ls

Afficher les fichiers du répertoire home.

-ls -la

Afficher tous les fichiers et comprendre les fichiers cachés.

Récupérer le mot de passe :

Utiliser les commandes du shell alternatives pour au mot de passe.

Rechercher des fichiers ou des indices dans le répertoire home de bandit26.

Trier puis sortir de la session SSH.

Prochaine étape:

ssh bandit27@bandit.labs.overthewire.org -p 2220