Bandit Niveau 10 → 11

But:

Se connecter au niveau 10 et décoder une chaîne encodée en base64 pour obtenir le mot de passe du niveau 11.

Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit10
Mot de passe : [utiliser le mot de passe du niveau 9-10]
Fichier cible : Un fichier data.txtcontenant du texte encodé en base64

Objectif : Décodeur la chaîne base64 pour obtenir le mot de passe

Approche:

Je me connecte avec le mot de passe du niveau précédent. Un fichier data.txtcontient une chaîne de caractères encodée en base64. Je dois utiliser la commande base64 -dpour décoder cette et chaîne obtenir le mot de passe du niveau 11.

Concepts clés:

Utilisation de base64 -dpour décoder du texte
Comprendre l'encodage base64
Décoder les données pour obtenir des informations Lisibles
Combiner des commandes avec le pipe (|)

Commandes:

-ssh bandit10@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 10.

-ls -la

Afficher tous les fichiers du répertoire courant.

-cat data.txt

Afficher le contenu du fichier data.txtpour voir la chaîne encodée en base64.

Décodage du texte :

-base64 -d data.txt

Décoder le fichier data.txten base64 pour obtenir le mot de passe.

Ou :

-cat data.txt | base64 -d

La sortie affichera le mot de passe du niveau 11.

Filtrer 

-sortie

Sortir de la session SSH.

Prochaine étape

Utiliser ce mot de passe pour se connecter au niveau 11 :

ssh bandit11@bandit.labs.overthewire.org -p 2220