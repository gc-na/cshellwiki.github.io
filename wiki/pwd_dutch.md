# [Linux] Bash pwd gebruik: Toon de huidige werkdirectory

## Overzicht
De `pwd` (print working directory) opdracht in Bash toont het pad van de huidige werkdirectory waarin je je bevindt. Dit is handig om te weten waar je bent in de bestandsstructuur van het systeem.

## Gebruik
De basis syntaxis van de `pwd` opdracht is als volgt:

```bash
pwd [opties]
```

## Veelvoorkomende Opties
- `-L`: Toont het logische pad van de huidige werkdirectory, wat betekent dat het symlinks negeert.
- `-P`: Toont het fysieke pad van de huidige werkdirectory, waarbij alle symlinks worden gevolgd.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `pwd` opdracht:

1. Gewoon de huidige werkdirectory tonen:
   ```bash
   pwd
   ```

2. Het logische pad tonen (standaard gedrag):
   ```bash
   pwd -L
   ```

3. Het fysieke pad tonen (volg symlinks):
   ```bash
   pwd -P
   ```

## Tips
- Gebruik `pwd` vaak in combinatie met andere opdrachten om te bevestigen dat je in de juiste directory werkt.
- Als je werkt met symlinks, overweeg dan om de `-P` optie te gebruiken om het echte pad te zien.
- Vergeet niet dat de uitvoer van `pwd` altijd een absoluut pad is, wat betekent dat het begint vanaf de root directory.