Bandit Niveau 6 → 7
Objectifs

Se connecter au niveau 6 et trouver un fichier spécifique dans l'ensemble du système de fichiers avec des propriétés particulières (propriétaire bandit6, groupe bandit6, taille 33 bytes) pour obtenir le mot de passe du niveau 7.

Données d'information
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit6
Mot de passe : [utiliser le mot de passe du niveau 5-6]
Fichier cible : Un fichier appartenant à bandit6, groupe bandit6, taille 33 octets, stocké quelque part dans le système
Approche

Je me connecte avec le mot de passe du niveau précédent. Le fichier n'est pas dans le répertoire home, il est stocké quelque part dans le système de fichiers. Je dois utiliser findà partir de la racine (/) pour rechercher un fichier avec les caractéristiques spécifiques : propriétaire bandit6, groupe bandit6, et taille 33 octets.

Concepts clés
Utilisation de findsur l'ensemble du système
Recherche par propriétaire ( -user)
Recherche par groupe ( -group)
Recherche par taille exacte ( -size)
Suppression des erreurs de permissions ( 2>/dev/null)
Commandes

-ssh bandit6@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 6.

-find / -user bandit6 -group bandit6 -size 33c 2>/dev/null

Recherchez dans tout le système un fichier appartenant à bandit6, groupe bandit6, de taille 33 octets. Le 2>/dev/nullsupprimé les messages d'erreur de permissions.

Une fois connecté :

-cat [chemin_du_fichier_trouvé]

Lire le contenu du fichier trouvé pour obtenir le mot de passe du niveau 7.

Trier :

-sortie

Sortir de la session SSH.

Prochaine étape

Utiliser ce mot de passe pour se connecter au niveau 7 :

ssh bandit7@bandit.labs.overthewire.org -p 2220