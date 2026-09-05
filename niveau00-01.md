Bandit Level 0 → 1




 Objectifs:

Se connecter au serveur Bandit via SSH et trouver le mot de passe du niveau 1 dans le répertoire home.


 Informations données:

- Hôte : bandit.labs.overthewire.org
- Port : 2220
- Utilisateur : bandit0
- Mot de passe : bandit0
- Fichier cible : readme


Approche:

Je me connecte via SSH avec les identBandit Level 0 → 1


 Objectifs:

Se connecter au serveur Bandit via SSH et trouver le mot de passe du niveau 1 dans le répertoire home.


Approche:Je me connecte via SSH avec les identifiants fournis, puis j'explore le répertoire pour trouver le fichier `readme` qui contient le mot de passe.



Commandes:

-ssh bandit0@bandit.labs.overthewire.org -p 2220


-Se connecter au serveur Bandit sur le port 2220 avec l'utilisateur bandit0.


-ls -la

Afficher tous les fichiers du répertoire courant, y compris les fichiers cachés.


Une fois connecté :

cat readme


Lire le contenu du fichier readme pour obtenir le mot de passe du niveau 1.

 Sortir :

exit


Sortir de la session SSH.


 Prochaine étape:

Utiliser ce mot de passe pour se connecter au niveau 1 :

ssh bandit1@bandit.labs.overthewire.org -p 2220

