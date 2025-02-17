# [Linux] Bash lsof Utilisation : Afficher les fichiers ouverts par les processus

## Overview
La commande `lsof` (List Open Files) est utilisée pour afficher les fichiers ouverts par les processus sur un système Unix/Linux. Elle permet d'obtenir des informations sur les fichiers, les sockets et les périphériques utilisés par les applications en cours d'exécution.

## Usage
La syntaxe de base de la commande `lsof` est la suivante :

```bash
lsof [options] [arguments]
```

## Common Options
Voici quelques options courantes pour la commande `lsof` :

- `-u [utilisateur]` : Affiche les fichiers ouverts par un utilisateur spécifique.
- `-p [PID]` : Affiche les fichiers ouverts par un processus avec un identifiant spécifique (PID).
- `-i` : Montre les fichiers ouverts qui sont des connexions réseau.
- `+D [répertoire]` : Affiche les fichiers ouverts dans un répertoire spécifique et ses sous-répertoires.
- `-t` : Affiche uniquement les identifiants de processus (PID), sans autres informations.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `lsof` :

1. **Afficher tous les fichiers ouverts :**
   ```bash
   lsof
   ```

2. **Afficher les fichiers ouverts par un utilisateur spécifique :**
   ```bash
   lsof -u nom_utilisateur
   ```

3. **Afficher les fichiers ouverts par un processus spécifique :**
   ```bash
   lsof -p 1234
   ```

4. **Afficher les connexions réseau ouvertes :**
   ```bash
   lsof -i
   ```

5. **Afficher les fichiers ouverts dans un répertoire spécifique :**
   ```bash
   lsof +D /chemin/vers/répertoire
   ```

## Tips
- Utilisez `lsof` avec `grep` pour filtrer les résultats selon vos besoins, par exemple : 
  ```bash
  lsof | grep nom_fichier
  ```
- Pour obtenir des informations en temps réel, combinez `lsof` avec `watch` :
  ```bash
  watch lsof
  ```
- Soyez prudent lorsque vous utilisez `lsof` avec des options qui affichent beaucoup de données, car cela peut ralentir votre terminal.