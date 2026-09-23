Bandit Niveau 20 → 21

Objectifs:

Exécuter un setuid binaire qui se reconnecte à un port spécifique pour obtenir le mot de passe du niveau 21.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit20
Mot de passe : [utiliser le mot de passe du niveau 19-20]
Fichier cible : Un binaire setuid dans le répertoire home

Objectif : Exécuter le binaire qui se reconnecte et obtient le mot de passe

Approche:
Se connecter au niveau 20. Un binaire setuid est présent qui se reconnectera à localhost sur un port spécifique. D'abord, créez un serveur d'écoute sur ce port avec nc -l, puis exécuter le binaire qui se reconnectera et enverra le mot de passe du niveau 21.

Commandes:

-ssh bandit20@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 20.

-ls -la

Afficher les fichiers pour identifier le binaire.

Créer un serveur d'écoute :

-nc -l -p 4242

Écouter sur le port 4242 (adapter le numéro de port selon le binaire).

Puis dans un autre terminal :

-./[nom_du_binaire] 4242

Exécuter le binaire avec le numéro du port.

Le serveur d'écoute reçoit le mot de passe du niveau 21.

Trier puis sortir de la session SSH.

Prochaine étape:

ssh bandit21@bandit.labs.overthewire.org -p 2220