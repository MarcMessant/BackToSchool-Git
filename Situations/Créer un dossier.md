## Créer un dossier dans le repo Git

Git ne versionne que les fichiers, donc pour créer un dossier il faut créer au moins un fichier dedans.

### Étapes

1. **Aller dans le repo local :**
```bash
cd ton-repo
```

2. **Créer un dossier :**
```bash
mkdir mon_dossier
```

3. **Ajouter un fichier dedans (par exemple .gitkeep) :**
```bash
touch mon_dossier/.gitkeep
```

4. **Ajouter et commit :**
```bash
git add mon_dossier
git commit -m "Ajout du dossier mon_dossier"
```

5. **Envoyer sur GitHub :**
```bash
git push origin main
```
