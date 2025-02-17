# [Linux] Bash cmp gebruik: Vergelijk twee bestanden byte voor byte

## Overzicht
De `cmp`-opdracht in Bash wordt gebruikt om twee bestanden byte voor byte te vergelijken. Het geeft aan waar de bestanden verschillen en kan nuttig zijn voor het controleren van de integriteit van bestanden of het identificeren van wijzigingen.

## Gebruik
De basis syntaxis van de `cmp`-opdracht is als volgt:

```bash
cmp [opties] [bestanden]
```

## Veelvoorkomende opties
- `-l`: Toon de verschillen in octale notatie.
- `-s`: Stilte modus; geen uitvoer, maar geeft een exit-status terug.
- `-i OFFSET`: Begin de vergelijking bij een specifieke byte-offset.
- `-n N`: Vergelijk slechts de eerste N bytes van de bestanden.

## Veelvoorkomende voorbeelden

1. Vergelijk twee bestanden en toon de eerste byte waar ze verschillen:
   ```bash
   cmp bestand1.txt bestand2.txt
   ```

2. Vergelijk twee bestanden in stilte modus:
   ```bash
   cmp -s bestand1.txt bestand2.txt
   ```

3. Vergelijk de eerste 10 bytes van twee bestanden:
   ```bash
   cmp -n 10 bestand1.txt bestand2.txt
   ```

4. Vergelijk twee bestanden en toon de verschillen in octale notatie:
   ```bash
   cmp -l bestand1.txt bestand2.txt
   ```

## Tips
- Gebruik de `-s` optie als je alleen geïnteresseerd bent in de exit-status om te bepalen of de bestanden gelijk zijn.
- Combineer `cmp` met andere commando's zoals `grep` voor meer geavanceerde analyses van de uitvoer.
- Vergeet niet dat `cmp` alleen geschikt is voor binaire en tekstbestanden; het werkt niet goed met directories of andere types bestanden.