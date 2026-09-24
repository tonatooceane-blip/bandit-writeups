Bandit Level 31 → 32


Objectifs:

Cloner un dépôt Git, modifier le contenu et pousser les changements pour obtenir le mot de passe du niveau 32.

Informations données:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit31-git
Mot de passe : [utiliser le mot de passe du niveau 30-31]
Dépôt Git : ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo


Objectif : Modifier et pousser des changements Git


Approche:

Cloner le dépôt Git depuis sa machine locale. Lire les instructions dans le fichier README. Modifier les fichiers selon les instructions. Ajouter les changements à Git avec git add, faire un commit et pousser les changements avec git push. Le serveur répondra avec le mot de passe du niveau 32.

Commandes:

Sur ta machine locale :

-git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo

Cloner le dépôt Git.

-cd repo

Naviguer dans le répertoire.

-cat README.md

Lire les instructions du niveau.

Modifier et pousser :

-echo "contenu" > [fichier]

Créer ou modifier un fichier selon les instructions.

-git add .

Ajouter les changements à l'index.

-git commit -m "Message de commit"

Créer un commit avec les changements.

-git push origin main

Pousser les changements au serveur.

Le serveur retournera le mot de passe du niveau 32.

Prochaine étape:

ssh bandit32@bandit.labs.overthewire.org -p 2220