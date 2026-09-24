Bandit Level 29 → 30


Objectifs:

Cloner un dépôt Git et explorer les branches pour obtenir le mot de passe du niveau 30.

Informations données:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit29-git
Mot de passe : [utiliser le mot de passe du niveau 28-29]
Dépôt Git : ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo


Objectif : Cloner et explorer les branches Git:


Approche:

Cloner le dépôt Git depuis sa machine locale. Explorer les fichiers du dépôt. Le mot de passe peut se trouver dans une branche différente. Utiliser git branch pour lister les branches et git checkout pour les explorer.

Commandes:

Sur ta machine locale, vérifie que Git est installé :

-git --version

Vérifier que Git est disponible.

Cloner le dépôt :

-git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo

Cloner le dépôt Git.

Lister les branches :

-cd repo

Naviguer dans le répertoire.

-git branch

Afficher les branches locales.

-git branch -a

Afficher toutes les branches (locales et distantes).

Explorer les branches :

-git checkout [nom_branche]

Passer à une autre branche.

-cat [fichier]

Lire les fichiers dans chaque branche pour chercher le mot de passe.

-git checkout main

Retourner à la branche principale.

Prochaine étape:

ssh bandit30@bandit.labs.overthewire.org -p 2220