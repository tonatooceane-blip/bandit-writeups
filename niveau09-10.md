Bandit Niveau 9 → 10

Objectifs:

Se connecter au niveau 9 et extraire les chaînes de caractères Lisibles d'un fichier binaire en utilisant stringspour obtenir le mot de passe du niveau 10.

Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit9
Mot de passe : [utiliser le mot de passe du niveau 8-9]
Fichier cible : Un fichier data.txtcontenant des données binaires
Objectif : Extraire les chaînes de caractères lisibles précédées de plusieurs signes égaux (=)

Approche:

Je me connecte avec le mot de passe du niveau précédent. Un fichier data.txtcontient des données binaires et du texte mélangé. Je dois utiliser stringspour extraire toutes les chaînes de caractères lisibles (ASCII), puis filtrer celles qui commencent par plusieurs signes égaux (=) pour trouver le mot de passe.

Concepts clés:
Utilisation de stringspour extraire du texte lisible de fichiers binaires
Filtrage des chaînes de caractères avecgrep
Combiner plusieurs commandes avec le pipe (|)
Travailler avec des fichiers mixtes (binaires + texte)

Commandes:

-ssh bandit9@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 9.

-ls -la

Afficher tous les fichiers du répertoire courant.

-chaînes de données.txt

Extraire toutes les chaînes de caractères lisibles du fichier data.txt.

Filtrage des chaînes possibles :

-strings data.txt | grep "="

Extraire les chaînes Lisibles et filtrer celles contenant "==" pour trouver le mot de passe du niveau 10.

Filtrer :

-sortie

Sortir de la session SSH.

Prochaine étape

Utiliser ce mot de passe pour se connecter au niveau 10 :

ssh bandit10@bandit.labs.overthewire.org -p 2220