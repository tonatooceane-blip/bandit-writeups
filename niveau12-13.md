Bandit Niveau 12 → 13

Objectifs:

Décoder un hexdump et décompresser les fichiers imbriqués pour obtenir le mot de passe.

Données d'information:

Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit12
Mot de passe : [utiliser le mot de passe du niveau 11-12]
Fichier cible : data.txt (hexdump)

Approche:

Créez un répertoire temporaire, copiez data.txt, décoder l'hexdump avec xxd -r, puis identifiez et décompressez les fichiers imbriqués avec file.

Commandes:

-ssh bandit12@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 12.

-mktemp -d

Créer un répertoire temporaire.

-cp data.txt /tmp/[répertoire]/

Copier le fichier.

-cd /tmp/[répertoire]/

Naviguer dans le répertoire.

-xxd -r data.txt > data

Décoder l'hexdump.

Décompression :

-données du fichier

Vérifiez le type de compression.

-gunzip données

Décompresser gzip.

-bzip2 -d données.bz2

Décompresseur bzip2.

-tar -xf données.tar

Extraire une archive goudron.

Répéter jusqu'à trouver le mot de passe en texte clair.

Trier :

-sortie

Sortir de la session SSH.

Prochaine étape:

ssh bandit13@bandit.labs.overthewire.org -p 2220