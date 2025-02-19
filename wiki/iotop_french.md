# [Linux] C Shell (csh) iotop : surveiller l'utilisation du disque par les processus

## Overview
La commande `iotop` permet de surveiller l'utilisation des entrées/sorties (I/O) des processus en temps réel sur un système Linux. Elle affiche les processus qui consomment le plus de ressources I/O, ce qui peut être utile pour diagnostiquer des problèmes de performance liés au disque.

## Usage
La syntaxe de base de la commande `iotop` est la suivante :

```bash
iotop [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `iotop` :

- `-o` : Affiche uniquement les processus qui effectuent des opérations I/O.
- `-b` : Exécute `iotop` en mode batch, utile pour les scripts.
- `-n NUM` : Définit le nombre d'itérations à afficher avant de quitter.
- `-d SEC` : Définit l'intervalle de mise à jour en secondes.

## Common Examples
Voici quelques exemples pratiques de l'utilisation de `iotop` :

1. **Afficher tous les processus I/O :**
   ```bash
   iotop
   ```

2. **Afficher uniquement les processus qui effectuent des opérations I/O :**
   ```bash
   iotop -o
   ```

3. **Exécuter `iotop` en mode batch pour 10 itérations :**
   ```bash
   iotop -b -n 10
   ```

4. **Définir un intervalle de mise à jour de 2 secondes :**
   ```bash
   iotop -d 2
   ```

## Tips
- Utilisez l'option `-o` pour filtrer les processus inactifs et vous concentrer sur ceux qui consomment des ressources.
- En mode batch, redirigez la sortie vers un fichier pour une analyse ultérieure, par exemple : `iotop -b -n 10 > iotop_output.txt`.
- Vérifiez régulièrement l'utilisation I/O pour identifier les goulets d'étranglement potentiels dans les performances de votre système.