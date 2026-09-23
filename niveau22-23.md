Bandit Niveau 22 → 23

Objectifs:

Analyser le script shell exécuté par la tâche Cron pour comprendre son fonctionnement et obtenir le mot de passe du niveau 23.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit22
Mot de passe : [utiliser le mot de passe du niveau 21-22]
Fichier cible : Tâches Cron et script shell

Objectif : Analyser le script pour obtenir le mot de passe

Approche:

Se connecter au niveau 22. Une tâche Cron exécute un script shell. Consultez /etc/cron.d/ pour identifier le script. Analyser le script pour comprendre comment il fonctionne. Le script est volontairement facile à lire. Exécuter le script ou modifier ses paramètres pour obtenir le mot de passe du niveau 23.

Commandes:

-ssh bandit22@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 22.

-ls -la /etc/cron.d/

Afficher les fichiers de cron.

Examiner la tâche cron :

-cat /etc/cron.d/[fichier_cron]

Lisez le fichier de configuration pour identifier le script.

-cat [chemin_du_script]

Analyser le script shell pour comprendre son fonctionnement.

Exécuter ou adapter le script :

-bash [chemin_du_script] [paramètre]

Exécuter le script en modifiant les paramètres selon ce qu'on a appris.

Ou analyser le script pour découvrir où il stocke le mot de passe.

Filtrer puis sortir de la session SSH.

Prochaine étape

ssh bandit23@bandit.labs.overthewire.org -p 2220