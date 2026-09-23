Bandit Niveau 28 → 29

Objectifs:

Cloner un dépôt Git et explorer son historique pour obtenir le mot de passe du niveau 29.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit28-git
Mot de passe : [utiliser le mot de passe du niveau 27-28]
Dépôt Git : ssh://bandit28- git@bandit.labs.overthewire.org /home/bandit28-git/repo


Objectif : Cloner et explorer l'historique Git

Approche:

Cloner le dépôt Git depuis sa machine locale. Explorer les fichiers du dépôt. Le mot de passe peut se trouver dans les fichiers actuels ou dans l'historique Git. Utiliser git loget git showpour explorer les commits précédents.

Commandes:

Sur la machine locale, vérifiez que Git est installé :

-git --version

Vérifiez que Git est disponible.

Cloner le dépôt :

-git clone ssh://bandit28-git@bandit.labs.overthewire.org : 2220/home/bandit28-git/repo

Cloner le dépôt Git.

Explorer le dépôt :

-cd dépôt

Naviguer dans le répertoire.

-ls -la

Afficher les fichiers.

-chat [fichier]

Lire un fichier pour rechercher des indices.

Explorer l'historique Git :

-git log

Afficher l'historique des commits.

-git log --oneline

Afficher un résumé des commits.

-git afficher [commit]

Afficher les détails d'un engagement spécifique.

Ou :

-git diff [commit1] [commit2]

Comparez deux commits pour voir les modifications.

Prochaine étape:

ssh bandit29@bandit.labs.overthewire.org -p 2220