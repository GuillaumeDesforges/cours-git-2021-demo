# Handout: quelques commandes git

Commandes:

- `git config`: configure git sur votre ordinateur
- `git init`: initialise le dossier actuel comme un repository local git
- `git status`: indique l'état de git dans le dossier actuel
- `git add <path>`: ajoute un fichier à l'index
- `git rm --cached <path>`: enlève un fichier de l'index (sans le supprimer réellement)
- `git commit -m "<description>"`: crée un commit à partir de l'index actuel
- `git log`: affiche l'historique
- `git log --all`: affiche l'historique complet
- `git log --all --graph --oneline`: affiche l'historique complet joliment
- `git reset <ref>`: fait que l'index ressemble à la version `<ref>`
- `git reset --hard <ref>`: fait que les fichiers locaux ressemblent à `<ref>` et que la branche actuelle pointe vers `<ref>`
- `git checkout <ref>`: fait pointer `HEAD` vers `<ref>` et mets à jour les fichiers locaux
- `git branch <branch>`: crée une nouvelle branche nommée `<branch>`
- `git branch`: liste les branches
- `git branch -vv`: liste les branches avec plus d'info
- `git branch -d <branch>`: supprime une branche
- `git merge <branch>`: merge la branche distante nommée `<branch>` vers la branche actuelle
- `git clone <url>`: crée un dossier avec pour remote `origin` l'url donnée
- `git push -u origin HEAD`: envoie la branche actuelle vers le remote `origin`
- `git push`: met à jour la branche actuelle vers le remote `origin`
- `git fetch`: met à jour la copie des branches distantes
- `git merge FETCH_HEAD`: merge la branche distante associée à la branche actuelle
- `git pull`: raccourci pour `git fetch` puis `git merge FETCH_HEAD`
- `git pull --ff-only`: raccourci pour `git fetch` puis `git merge FETCH_HEAD`, mais ne merge automatiquement que si c'est un fast-forward

> A toute commande on peut ajouter l'option `--help` pour savoir ce qu'elle fait et comment l'utiliser.
> Par exemple: `git merge --help`

Description des paramètres:

- `<path>`: chemin relatif vers un fichier
- `<ref>`: id de commit ou nom de branche
- `<branch>`: nom de branche
- `<remote>`: nom de remote
- `<url>`: url de remote
