Bandit Niveau 27 → 28

Objectifs

Cloner un dépôt Git accessible en SSH pour obtenir le mot de passe du niveau 28.

Données d'information
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit27-git
Mot de passe : [utiliser le mot de passe du niveau 26-27]
Dépôt Git : ssh://bandit27- git@bandit.labs.overthewire.org /home/bandit27-git/repo
Objectif : Cloner le dépôt pour obtenir le mot de passe
Approche

Il existe un dépôt Git accessible en SSH. Le mot de passe pour au dépôt est le même que celui de l'utilisateur bandit27. Cloner le dépôt depuis sa machine locale et explorer son contenu pour trouver le mot de passe du niveau 28.

Commandes:

Sur la machine locale (pas SSH), vérifiez que Git est installé :

-git --version

Vérifiez que Git est disponible.

Cloner le dépôt :

-git clone ssh://bandit27-git@bandit.labs.overthewire.org : 2220/home/bandit27-git/repo

Cloner le dépôt Git. Utiliser le mot de passe du niveau 27 lorsque demandé.

Explorer le dépôt :

-cd dépôt

Naviguer dans le répertoire du dépôt.

-ls -la

Afficher les fichiers du dépôt.

-chat [fichier]

Lire les fichiers pour trouver le mot de passe du niveau 28.

Prochaine étape:

ssh bandit28@bandit.labs.overthewire.org -p 2220