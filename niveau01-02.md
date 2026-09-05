Bandit Niveau 1 → 2

-Objectifs:

Se connecter au niveau 1 et lire un fichier nommé "-" (tiret) pour obtenir le mot de passe du niveau 2.

-Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit1
Mot de passe : [utiliser le mot de passe du niveau 0-1]
Fichier cible : - (tiret)



-Approche:

Je me connecte avec le mot de passe du niveau précédent. Le fichier "-" a un nom spécial qui peut être problématique à lire. Je dois utiliser une approche spéciale pour à ce fichier.

-Concepts clés:

Fichiers avec noms spéciaux ou problématiques
Utilisation de chemins relatifs (./)
Redirection d'entrée (<)

-Commandes:

-ssh bandit1@bandit.labs.overthewire.org -p 2220

-Se connecter au niveau 1.

-ls -la

-Afficher les fichiers du répertoire courant pour voir le fichier "-".

Une fois connecté :

cat ./-

Lisez le contenu du fichier "-" en utilisant le chemin relatif "./". Le tiret est interprété comme une option sans le "./" devant.

Trier et taper:

exit

Sortir de la session SSH.

Prochaine étape:

Utiliser ce mot de passe pour se connecter au niveau 2 :

Taper:
ssh bandit2@bandit.labs.overthewire.org -p 2220