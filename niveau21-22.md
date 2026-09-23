Bandit Niveau 21 → 22

Objectifs:

Explorer les tâches Cron dans /etc/cron.d/ pour identifier quelle commande s'exécute automatiquement et obtenir le mot de passe du niveau 22.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit21
Mot de passe : [utiliser le mot de passe du niveau 20-21]
Fichier cible : Tâches Cron dans /etc/cron.d/

Objectif : Identifier la tâche cron et obtenir le mot de passe

Approche:

Se connecter au niveau 21. Un programme s'exécute automatiquement à intervalles réguliers grâce à cron. Consultez les fichiers dans /etc/cron.d/ pour voir la configuration et identifier la commande exécutée. Suivre le chemin du script ou de la commande pour découvrir comment il obtient le mot de passe.

Commandes:

-ssh bandit21@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 21.

-ls -la /etc/cron.d/

Afficher les fichiers de cron disponibles.

Examiner les tâches cron :

-cat /etc/cron.d/[fichier_cron]

Lisez le fichier de configuration cron pour voir la commande exécutée.

Ou :

-cat /etc/cron.d/cronjobs

Chercher le script ou la commande qui s'exécute pour le niveau 21.


-cat [chemin_du_script]

Examiner le script pour comprendre comment il obtient le mot de passe du niveau 22.

Trier puis sortir de la session SSH.

Prochaine étape:

ssh bandit22@bandit.labs.overthewire.org -p 2220