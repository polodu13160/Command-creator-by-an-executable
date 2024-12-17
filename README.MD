# Script d'installation pour créer une commande personnalisée

Ce script vous permet de transformer n'importe quel fichier exécutable en une commande utilisable depuis votre terminal en quelques étapes simples.

## Fonctionnalités

1. Copie un fichier exécutable (Python, Bash, etc.) dans le dossier `~/scripts`.
2. Rend le fichier exécutable.
3. Crée un alias dans votre configuration Zsh (`~/.zshrc`) pour exécuter facilement le fichier depuis le terminal.

## Utilisation

1. Lancez le script depuis votre terminal :
   ```bash
   ./convertissor.sh
   ```

2. Répondez aux questions posées :
   - **Chemin du fichier exécutable** : Entrez le chemin absolu ou relatif du fichier que vous souhaitez transformer en commande.
   - **Nom de l'exécutable** : Indiquez le nom sous lequel le fichier sera enregistré dans `~/scripts`.
   - **Nom de l'alias** : Spécifiez le nom de la commande que vous souhaitez utiliser.

3. Rechargez la configuration Zsh pour activer l'alias immédiatement :
   ```bash
   source ~/.zshrc
   ```

## Exemple

Si vous voulez transformer un script Python `convert_html_to_md.py` situé dans `~/Documents` en une commande `converthtmltomd`, voici le processus :

- Entrez le chemin : Exemple : `/home/votre_utilisateur/Documents/convert_html_to_md.py`.
- Entrez le nom de l'exécutable : `converthtmltomd`.
- Entrez le nom de l'alias : `converthtmltomd`.

Après exécution, vous pourrez utiliser votre script directement en tapant :  
```bash
converthtmltomd
```

## Remarques

- Le dossier `~/scripts` est automatiquement créé si nécessaire.
- Si l'alias existe déjà dans `~/.zshrc`, il ne sera pas écrasé.
- Pour activer un nouvel alias sans redémarrer votre terminal, exécutez :
  ```bash
  source ~/.zshrc
  ```

## Dépendances

- **Shell Zsh** (le script ajoute un alias dans `~/.zshrc`).
- Les permissions suffisantes pour copier des fichiers et modifier la configuration Zsh.

--- 

Ce fichier `.md` contient tout ce qu'il faut pour comprendre et utiliser le script. 😊
