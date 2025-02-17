# [Linux] Bash groupmod : Modifier les groupes d'utilisateurs

## Overview
La commande `groupmod` est utilisée pour modifier les attributs d'un groupe d'utilisateurs dans un système Linux. Elle permet d'ajuster des paramètres tels que le nom du groupe ou son identifiant (GID).

## Usage
La syntaxe de base de la commande `groupmod` est la suivante :

```bash
groupmod [options] [arguments]
```

## Common Options
Voici quelques options courantes pour `groupmod` :

- `-n, --new-name <nom>` : Change le nom du groupe.
- `-g, --gid <GID>` : Modifie l'identifiant de groupe (GID).
- `-o` : Permet de définir un GID non unique (par défaut, les GID doivent être uniques).

## Common Examples

### Changer le nom d'un groupe
Pour changer le nom d'un groupe de `ancien_nom` à `nouveau_nom`, utilisez la commande suivante :

```bash
groupmod -n nouveau_nom ancien_nom
```

### Modifier l'identifiant de groupe
Pour changer le GID d'un groupe de `1001` à `1002`, utilisez :

```bash
groupmod -g 1002 nom_du_groupe
```

### Changer le nom et le GID d'un groupe
Pour changer à la fois le nom et le GID d'un groupe, vous pouvez combiner les options :

```bash
groupmod -n nouveau_nom -g 1002 ancien_nom
```

## Tips
- Assurez-vous d'avoir les droits d'administrateur (root) pour exécuter `groupmod`.
- Vérifiez les groupes existants avec la commande `getent group` avant de faire des modifications.
- Utilisez `groupmod` avec précaution, car des modifications incorrectes peuvent affecter l'accès des utilisateurs aux ressources du système.