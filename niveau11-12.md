Bandit Niveau 11 → 12

*Objectifs:

Se connecter au niveau 11 et déchiffrer une chaîne encodée avec ROT13 pour obtenir le mot de passe du niveau 12.

*Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit11
Mot de passe : [utiliser le mot de passe du niveau 10-11]
Fichier cible : Un fichier data.txtcontenant du texte chiffré avec ROT13
Objectif : Déchiffrer la chaîne ROT13 pour obtenir le mot de passe

*Approche:

Je me connecte avec le mot de passe du niveau précédent. Un fichier data.txtcontient une chaîne de caractères chiffrée avec ROT13 (rotation de 13 positions dans l'alphabet). Je dois utiliser la commande trpour décoder cette et chaîne obtenir le mot de passe du niveau 12.

*Concepts clés:

Utilisation de trpour transformer des caractères
Comprendre le chiffre ROT13
Décodeur les données chiffrées pour obtenir des informations lisibles
Combiner des commandes avec le pipe (|)

*Commandes:

-ssh bandit11@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 11.

-ls -la

Afficher tous les fichiers du répertoire courant.

-cat data.txt

Afficher le contenu du fichier data.txtpour voir la chaîne chiffrée en ROT13.

Déchiffrement du texte :

-tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt

Déchiffrer le fichier data.txten utilisant ROT13 pour obtenir le mot de passe.

Ou :

-cat données.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

La sortie affichera le mot de passe du niveau 12.

*Trier :

-sortie

Sortir de la session SSH.

*Prochaine étape

Utiliser ce mot de passe pour se connecter au niveau 12 :

ssh bandit12@bandit.labs.overthewire.org -p 2220