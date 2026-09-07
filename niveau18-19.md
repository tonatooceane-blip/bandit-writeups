Bandit Niveau 18 → 19

Objectifs:

Lire le fichier readme dans le répertoire personnel avant la déconnexion automatique pour obtenir le mot de passe du niveau 19.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit18
Mot de passe : [utiliser le mot de passe du niveau 17-18]
Fichier cible : readme dans le répertoire home
Problème : Le fichier .bashrc se déconnecte automatiquement de l'utilisateur

Approche:

Se connecter au niveau 18. Le fichier .bashrc a été modifié pour se déconnecter automatiquement. Il faut exécuter la commande pour lire le fichier readme immédiatement après la connexion avant la déconnexion.

Commandes:

-ssh bandit18@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 18.

Exécuter immédiatement la commande :

-cat readme

Ou en une seule commande :

-ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme

Se connecter et lire le fichier readme en une seule commande avant la déconnexion automatique.

Trier :

La déconnexion se fera automatiquement.

Prochaine étape:

ssh bandit19@bandit.labs.overthewire.org -p 2220