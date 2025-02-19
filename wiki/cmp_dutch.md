# [Linux] C Shell (csh) cmp gebruik: Vergelijk bestanden byte voor byte

## Overzicht
De `cmp` opdracht in C Shell (csh) wordt gebruikt om twee bestanden byte voor byte te vergelijken. Het geeft aan waar de bestanden verschillen, wat nuttig kan zijn voor het controleren van de integriteit van bestanden of het vinden van wijzigingen.

## Gebruik
De basis syntaxis van de `cmp` opdracht is als volgt:

```csh
cmp [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-l`: Toon de verschillen in hexadecimale vorm.
- `-s`: Stil; geen uitvoer, alleen een exit-status.
- `-i OFFSET`: Begin de vergelijking bij een specifieke offset.
- `-n NUM`: Vergelijk slechts de eerste NUM bytes van de bestanden.

## Veelvoorkomende Voorbeelden

1. Vergelijk twee bestanden en toon de eerste byte waar ze verschillen:
   ```csh
   cmp bestand1.txt bestand2.txt
   ```

2. Vergelijk twee bestanden stil en controleer de exit-status:
   ```csh
   cmp -s bestand1.txt bestand2.txt
   ```

3. Vergelijk de eerste 100 bytes van twee bestanden:
   ```csh
   cmp -n 100 bestand1.txt bestand2.txt
   ```

4. Vergelijk twee bestanden en toon de verschillen in hexadecimale vorm:
   ```csh
   cmp -l bestand1.txt bestand2.txt
   ```

## Tips
- Gebruik de `-s` optie als je alleen geïnteresseerd bent in de exit-status om te weten of de bestanden gelijk zijn of niet.
- Combineer `cmp` met andere commando's zoals `grep` voor geavanceerdere analyses van de uitvoer.
- Zorg ervoor dat je de juiste bestandsnamen en paden opgeeft om fouten te voorkomen.