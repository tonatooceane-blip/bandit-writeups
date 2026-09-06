Bandit Niveau 5 → 6
Objectifs

Se connecter au niveau 5 et trouver un fichier spécifique parmi plusieurs fichiers avec des propriétés particulières (lisibles, appartenant à bandit5, de taille réduite) pour obtenir le mot de passe du niveau 6.

Données d'information
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit5
Mot de passe : [utiliser le mot de passe du niveau 4-5]
Fichier cible : Un fichier lisible, appartenant à l'utilisateur bandit5, de taille réduite dans le répertoireinhere
Approche

Je me connecte avec le mot de passe du niveau précédent. Le répertoire inherecontient plusieurs fichiers et répertoires avec des propriétés différentes. Je dois utiliser findpour rechercher un fichier avec les caractéristiques spécifiques : Lisible, appartenant à Bandit5, et de taille réduite.

Concepts clés
Utilisation de findpour rechercher des fichiers
Recherche par propriétaire du fichier
Recherche par taille de fichier
Permissions des fichiers sous Linux
Commandes

-ssh bandit5@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 5.

-ls -la

Afficher tous les fichiers du répertoire courant.

-cd ici

Naviguer dans le répertoire inhere.

-ls -la

Afficher tous les fichiers et répertoires.

-trouver . -type f -propriétaire bandit5 -taille -1033c

Recherchez un fichier appartenant à bandit5 et de taille inférieure à 1033 octets.

Une fois connecté :

-cat [nom_du_fichier_trouvé]

Lire le contenu du fichier trouvé pour obtenir le mot de passe du niveau 6.

Trier :

-sortie

Sortir de la session SSH.

Prochaine étape

Utiliser ce mot de passe pour se connecter au niveau 6 :

ssh bandit6@bandit.labs.overthewire.org -p 2220