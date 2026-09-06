Bandit Niveau 2 → 3

Objectifs:

Se connecter au niveau 2 et lire un fichier dont le nom contient des espaces pour obtenir le mot de passe du niveau 3.

Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit2
Mot de passe : [utiliser le mot de passe du niveau 1-2]
Fichier cible : Un fichier avec des espaces dans le nom


Approche:

Je me connecte avec le mot de passe du niveau précédent. Un fichier avec des espaces dans son nom est présent. Sous Linux, les espaces dans les noms de fichiers peuvent être problématiques. Je dois utiliser des guillemets ou des antislash pour accéder au fichier.

Concepts clés:

-Fichiers avec des espaces dans le nom
-Utilisation de guillemets pour échapper aux espaces
-Utilisation d'antislash pour échapper aux caractères spéciaux
-Utilisation de tabulation pour l'auto-complétion

Commandes:

-ssh bandit2@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 2.

-ls -la

Afficher tous les fichiers du répertoire courant.

-cat "espaces dans ce nom de fichier"

Lire le contenu du fichier en utilisant des guillemets pour échapper aux espaces.

Une fois connecté :

Ou alternativement :

-cat espaces\ dans\ ce\ nom\ de\ fichier

Lire le contenu du fichier en utilisant des antislash pour échapper à chaque espace.

Trier :

-sortie

Sortir de la session SSH.

Prochaine étape

Utiliser ce mot de passe pour se connecter au niveau 3 :

ssh bandit3@bandit.labs.overthewire.org -p 2220