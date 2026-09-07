Bandit Niveau 19 → 20

Objectifs:

Exécuter un fichier binaire défini dans le répertoire personnel pour découvrir son fonctionnement et obtenir le mot de passe du niveau 20.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit19
Mot de passe : [utiliser le mot de passe du niveau 18-19]
Fichier cible : Un fichier binaire défini dans le répertoire home


Objectif : Exécuter le binaire pour découvrir son fonctionnement

Approche:

Se connecter au niveau 19. Un fichier binaire défini est présent dans le répertoire home. Exécuter ce fichier pour découvrir son fonctionnement. Il permettra d'accéder au mot de passe du niveau 20 stocké dans /etc/bandit_pass/bandit20.

Commandes:

-ssh bandit19@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 19.

-ls -la

Afficher les fichiers du répertoire pour identifier le binaire setuid.

Exécuter le binaire :

-./[nom_du_binaire]

Exécuter le fichier binaire sans arguments pour découvrir son fonctionnement.

Ou :

-./[nom_du_binaire] /etc/bandit_pass/bandit20

Exécuter avec le chemin du fichier de mot de passe si nécessaire.

Filtrer:

-sortie

Sortir de la session SSH.

Prochaine étape

ssh bandit20@bandit.labs.overthewire.org -p 2220