Bandit Niveau 8 → 9

Objectifs:
Se connecter au niveau 8 et trouver la ligne unique parmi plusieurs lignes (où toutes les autres lignes sont en double) pour obtenir le mot de passe du niveau 9.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit8
Mot de passe : [utiliser le mot de passe du niveau 7-8]
Fichier cible : Un fichier data.txtcontenant plusieurs lignes
Objectif : Trouver la ligne qui n'apparaît qu'une seule fois

Approche:

Je me connecte avec le mot de passe du niveau précédent. Un fichier data.txtcontient plusieurs lignes où la plupart sont des doublons. Une seule ligne est unique. Je dois utiliser sortpour trier les lignes et uniq -upour afficher uniquement les lignes qui n'apparaissent qu'une seule fois.

Concepts clés:

Utilisation de sortpour trier les lignes
Utilisation de uniq -upour afficher les lignes uniques
Combinaison de commandes avec le tuyau (|)
Filtrer les doublons

Commandes:

-ssh bandit8@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 8.

-ls -la

Afficher tous les fichiers du répertoire courant.

-sort data.txt | uniq -u

Trier le fichier et afficher uniquement la ligne qui n'apparaît qu'une seule fois.

Filtrage des doublons :

-cat data.txt | trier | uniq -u

Ou directement :

-sort data.txt | uniq -u

La sortie affichera la ligne unique qui est le mot de passe du niveau 9.

Trier :

-sortie

Sortir de la session SSH.

Prochaine étape

Utiliser ce mot de passe pour se connecter au niveau 9 :

ssh bandit9@bandit.labs.overthewire.org -p 2220