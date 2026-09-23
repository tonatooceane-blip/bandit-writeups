Bandit Niveau 25 → 26

Objectifs:

Découvrez quel shell utilise l'utilisateur bandit26 et comment fonctionner avec ce shell alternatif pour obtenir le mot de passe du niveau 26.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit25
Mot de passe : [utiliser le mot de passe du niveau 24-25]
Cible : Utilisateur bandit26 avec un shell alternatif


Objectif : Découvrir et utiliser le shell alternatif

Approche:

Se connecter au niveau 25. Essayer de se connecter à bandit26 devrait être simple, mais le shell de cet utilisateur n'est pas /bin/bash. Vérifiez dans /etc/passwd quel shell bandit26 utilise. Découvrez comment fonctionne ce shell et comment l'utiliser. Le shell alternatif permettra d'obtenir le mot de passe du niveau 26.

Commandes:

-ssh bandit25@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 25.

Découvrez le shell de bandit26 :

-cat /etc/passwd | grep bandit26

Affichez la ligne de bandit26 pour voir quel shell il utilise.

-ssh bandit26@bandit.labs.overthewire.org -p 2220

Connectez-vous à bandit26 pour découvrir le shell en action.

Utiliser le shell alternatif :

Une fois connecté avec le shell alternatif, découvrez comment utiliser les commandes de ce shell pour lire le mot de passe dans /etc/bandit_pass/bandit26.

Utiliser les commandes suggérées : ssh, cat, more, vi, ls, id, pwd

Filtrer puis sortir de la session SSH.

Prochaine étape

ssh bandit26@bandit.labs.overthewire.org -p 2220