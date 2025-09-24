## 1️. Configuration initiale
```bash
git config --global user.name "Ton Nom"
git config --global user.email "ton.email@example.com"
git config --global core.editor "code --wait"  # Définit VSCode comme éditeur par défaut
git config --list  # Vérifie la configuration
```

## 2. Création et clonage de dépôt
```bash
git init                   # Crée un dépôt local dans le dossier courant
git clone <url_du_repo>    # Clone un dépôt distant sur ton PC
```

## 3. Suivi et ajout de fichiers
```bash
git status                 # Affiche l'état des fichiers (modifiés, non suivis, staged)
git add <fichier>          # Ajoute un fichier pour le prochain commit
git add .                  # Ajoute tous les fichiers modifiés/non suivis
git rm <fichier>           # Supprime un fichier du dépôt (et du disque si nécessaire)
git mv <ancien> <nouveau>  # Renomme ou déplace un fichier

Astuce : Si tu as renommé un fichier directement sur GitHub et pas localement, git mv peut résoudre le décalage.
```

## 4. Validation des changements
```bash
git commit -m "Message du commit"  # Commit avec un message
git commit                       # Commit sans message → ouvre l’éditeur
```

## 5. Gestion du dépôt distant
```bash
git remote -v               # Liste les dépôts distants
git push origin main        # Pousse les commits locaux vers GitHub
git pull origin main        # Récupère les changements du dépôt distant

Si push rejeté :
! [rejected] main -> main (fetch first)
Solution : git pull --rebase origin main ou git fetch puis git merge.
```

## 6. Branches et fusion
```bash
git branch                  # Liste les branches locales
git branch <nom>            # Crée une branche
git checkout <nom>          # Change de branche
git switch <nom>            # Alternative moderne à checkout
git merge <branche>         # Fusionne une branche dans la branche courante
git rebase <branche>        # Rejoue tes commits sur une autre branche
```

## 7. Historique et annulation
```bash
git log                     # Affiche l’historique des commits
git diff                    # Affiche les changements non commités
git reset <fichier>         # Retire un fichier de la zone staging
git reset --hard <commit>   # Reviens à un commit précis (attention, destructif)
git checkout -- <fichier>   # Annule les modifications locales sur un fichier
```

## 8. Résolution de conflits
```bash
Lors d’un merge, si conflit :
Git marque les fichiers en conflit (<<<<<<<, =======, >>>>>>>).
Modifier les fichiers pour résoudre le conflit.
git add <fichier> pour marquer comme résolu.
git commit pour finaliser le merge.

Astuce : Pour éviter que VSCode s’ouvre à chaque merge, configure ton éditeur par défaut.
```

## 9. Astuces utiles
```bash
git fetch                  # Récupère les changements du distant sans merger
git log --oneline --graph  # Vue compacte de l’historique avec graph
git status -s              # Vue courte du status
```
