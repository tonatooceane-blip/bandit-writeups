Bandit Niveau 4 → 5
Objectifs

Se connecter au niveau 4 et trouver le bon fichier parmi plusieurs fichiers avec des noms bizarres pour obtenir le mot de passe du niveau 5.

Données d'information
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit4
Mot de passe : [utiliser le mot de passe du niveau 3-4]
Fichier cible : Un fichier lisible en texte dans le répertoire inhere(parmi plusieurs fichiers avec des noms bizarres)
Approche

Je me connecte avec le mot de passe du niveau précédent. Un répertoire inherecontient plusieurs fichiers avec des noms spéciaux commençant par des tirets. Je dois utiliser filepour identifier quel fichier est en texte lisible, puis le lire.

Concepts clés
Fichiers avec des noms spéciaux commençant par des tirets
Utilisation de filepour vérifier le type de fichier
Différencier les fichiers binaires des fichiers texte
Commandes

-ssh bandit4@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 4.

-ls -la

Afficher tous les fichiers du répertoire courant.

-cd ici

Naviguer dans le répertoire inhere.

-ls -la

Afficher tous les fichiers du répertoire inhere.

-déposer ./*

Afficher le type de chaque fichier pour identifier lequel est un fichier texte.

Une fois connecté :

-cat ./[nom_du_fichier_texte]

Lire le contenu du fichier texte pour obtenir le mot de passe du niveau 5.

Trier :

-sortie

Sortir de la session SSH.

Prochaine étape

Utiliser ce mot de passe pour se connecter au niveau 5 :

ssh bandit5@bandit.labs.overthewire.org -p 2220