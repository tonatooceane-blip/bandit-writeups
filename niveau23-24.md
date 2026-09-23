Bandit Niveau 23 → 24

Objectifs:

Créez un script shell personnalisé et le placer dans le répertoire Cron pour qu'il s'exécute automatiquement et obtient le mot de passe du niveau 24.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit23
Mot de passe : [utiliser le mot de passe du niveau 22-23]
Fichier cible : Tâches Cron et répertoire de scripts

Objectif : Créer un script shell pour obtenir le mot de passe

Approche:

Se connecter au niveau 23. Une tâche Cron exécute des scripts d'un répertoire spécifique. Consultez /etc/cron.d/ pour identifier le répertoire. Créer un script shell qui récupère le mot de passe du niveau 24. Placer ce script dans le répertoire approprié avec les bonnes permissions. Le script s'exécute automatiquement à intervalles réguliers.

Commandes:

-ssh bandit23@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 23.

-cat /etc/cron.d/[fichier_cron]

Identifier le répertoire où les scripts s'exécutent.

Créer un script shell :

-nano /tmp/myscript.sh

Créer un script shell temporaire.

frapper
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/output.txt

-chmod +x /tmp/myscript.sh

Rendre le script exécutable.

-cp /tmp/myscript.sh /var/spool/bandit-shell/[répertoire]/

Copier le script dans le répertoire Cron.

Attendre et récupérer le mot de passe :

-cat /tmp/output.txt

Une fois le script exécuté par Cron, récupérer le mot de passe.

Trier puis sortir de la session SSH.

Prochaine étape:

ssh bandit24@bandit.labs.overthewire.org -p 2220