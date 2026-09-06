Bandit Level 3 → 4


Objectifs

Se connecter au niveau 3 et trouver un fichier caché dans un répertoire pour obtenir le mot de passe du niveau 4.


nformations données

- Hôte: bandit.labs.overthewire.org
- Port: 2220
- Utilisateur: bandit3
- Mot de passe: [utiliser le password du niveau 2-3]
- Fichier cible : Un fichier caché dans le répertoire `inhere`


Approche

Je me connecte avec le mot de passe du niveau précédent. Un répertoire `inhere` contient un fichier caché. En Linux, les fichiers cachés commencent par un point (.). Je dois utiliser `ls -la` pour les voir.


Concepts clés

- Fichiers cachés en Linux (commençant par un point)
- Utilisation de `ls -la` pour afficher les fichiers cachés
- Navigation dans les répertoires (cd)


Commandes

-ssh bandit3@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 3.

-ls -la


Afficher tous les fichiers du répertoire courant, y compris les fichiers cachés.

-cd inhere

Naviguer dans le répertoire `inhere`.

-ls -la


Afficher tous les fichiers du répertoire `inhere` pour trouver le fichier caché.


Une fois connecté :

-cat [nom_du_fichier_caché]

Lire le contenu du fichier caché pour obtenir le mot de passe du niveau 4.

Sortir :

exit

Sortir de la session SSH.


Prochaine étape

Utiliser ce mot de passe pour se connecter au niveau 4 :


ssh bandit4@bandit.labs.overthewire.org -p 2220
