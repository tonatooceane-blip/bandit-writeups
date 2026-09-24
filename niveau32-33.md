Bandit Level 32 → 33


Objectifs:

Atteindre le point de contrôle d'achèvement du jeu de guerre Bandit et obtenir le message de victoire.

Informations données:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit32
Mot de passe : [utiliser le mot de passe du niveau 31-32]
Cible : Point de contrôle d'achèvement du jeu de guerre


Objectif : Terminer le jeu de guerre Bandit


Approche:

Se connecter au niveau 32. À ce stade, tu as exploré git, les shells, les tâches cron, les scripts, le port scanning, le SSL/TLS et bien d'autres concepts. Le niveau 32 est le dernier niveau du jeu de guerre officiel. Accéder au mot de passe du niveau 33 (le point de contrôle final) et recevoir le message de félicitations.

Commandes:

-ssh bandit32@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 32.

-cat /etc/bandit_pass/bandit33

Lire le mot de passe du niveau 33 (dernier niveau).

Ou :

-ssh bandit33@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 33 pour voir le message de fin.

Résultat :

Le serveur affichera un message : "À l'heure actuelle, le niveau 34 n'existe pas encore."

Cela signifie que tu as atteint la fin du jeu de guerre Bandit. Le niveau 33 est actuellement le dernier niveau disponible.

Prochaines étapes

🎉 Bravo ! Tu as complété OverTheWire Bandit (niveaux 0-33) ! 🎉

Le niveau 34 n'existe pas encore sur la plateforme. D'autres jeux de guerre OverTheWire (Natas, Leviathan, Krypton, Narnia…) pourraient être explorés ensuite.