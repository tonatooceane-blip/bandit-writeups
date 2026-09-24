Bandit Level 30 → 31


Objectifs:

Cloner un dépôt Git et explorer les tags pour obtenir le mot de passe du niveau 31.

Informations données:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit30-git
Mot de passe : [utiliser le mot de passe du niveau 29-30]
Dépôt Git : ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo


Objectif : Cloner et explorer les tags Git


Approche:

Cloner le dépôt Git depuis sa machine locale. Explorer les fichiers du dépôt. Le mot de passe peut se trouver dans un tag Git. Utiliser git tag pour lister les tags et git show pour voir leur contenu.

Commandes:

Sur ta machine locale, vérifie que Git est installé :

-git --version

Vérifier que Git est disponible.

Cloner le dépôt :

-git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo

Cloner le dépôt Git.

Lister les tags :

-cd repo

Naviguer dans le répertoire.

-git tag

Afficher les tags disponibles.

-git tag -l

Afficher tous les tags avec plus de détails.

Explorer les tags :

-git show [nom_tag]

Afficher le contenu d'un tag spécifique.

-git show [nom_tag]:[fichier]

Afficher le contenu d'un fichier dans un tag spécifique.

Chercher le mot de passe dans les tags.

Prochaine étape

ssh bandit31@bandit.labs.overthewire.org -p 2220