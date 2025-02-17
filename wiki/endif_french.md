# [Linux] Bash endif : Terminer une condition

## Overview
La commande `endif` est utilisée dans les scripts Bash pour marquer la fin d'une structure conditionnelle, généralement après une instruction `if`. Elle permet de structurer le code de manière lisible et de s'assurer que les blocs conditionnels sont correctement fermés.

## Usage
La syntaxe de base de la commande `endif` est la suivante :

```bash
endif
```

## Common Options
La commande `endif` n'a pas d'options spécifiques, car elle est principalement utilisée comme un mot-clé de fin dans les structures conditionnelles. Cependant, elle doit être utilisée en conjonction avec `if`, `then`, et d'autres mots-clés de contrôle de flux.

## Common Examples

### Exemple 1 : Utilisation de `if` avec `endif`
```bash
if [ "$USER" = "admin" ]; then
    echo "Bienvenue, administrateur."
endif
```

### Exemple 2 : Utilisation de `if` avec `else` et `endif`
```bash
if [ "$AGE" -lt 18 ]; then
    echo "Vous êtes mineur."
else
    echo "Vous êtes majeur."
endif
```

### Exemple 3 : Vérification d'un fichier
```bash
if [ -f "monfichier.txt" ]; then
    echo "Le fichier existe."
endif
```

## Tips
- Assurez-vous que chaque `if` a un `endif` correspondant pour éviter les erreurs de syntaxe.
- Utilisez des commentaires pour expliquer la logique de vos conditions, surtout dans des scripts complexes.
- Testez vos scripts dans un environnement sûr avant de les exécuter en production pour éviter des comportements inattendus.