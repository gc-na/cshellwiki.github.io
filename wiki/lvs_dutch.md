# [Linux] C Shell (csh) lvs gebruik: Toon logische volumenaam

## Overzicht
De `lvs` opdracht in C Shell (csh) wordt gebruikt om informatie weer te geven over de logische volumes in een Linux-systeem. Het biedt een overzicht van de beschikbare logische volumes en hun eigenschappen.

## Gebruik
De basis syntaxis van de `lvs` opdracht is als volgt:

```csh
lvs [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-o`: Specificeer welke velden moeten worden weergegeven.
- `-a`: Toon ook inactieve logische volumes.
- `--units`: Geef de eenheden aan voor de uitvoer, zoals MB of GB.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `lvs` opdracht:

1. Toon een lijst van alle logische volumes:
   ```csh
   lvs
   ```

2. Toon specifieke velden zoals naam, grootte en status:
   ```csh
   lvs -o lv_name,lv_size,lv_status
   ```

3. Toon ook inactieve logische volumes:
   ```csh
   lvs -a
   ```

4. Toon de logische volumes met een specifieke eenheid (bijvoorbeeld GB):
   ```csh
   lvs --units g
   ```

## Tips
- Gebruik de `-o` optie om alleen de informatie te tonen die je nodig hebt, dit maakt de uitvoer overzichtelijker.
- Combineer opties om meer gedetailleerde informatie te verkrijgen, zoals het tonen van inactieve volumes.
- Controleer regelmatig je logische volumes om ervoor te zorgen dat je systeem goed functioneert en om ruimteproblemen te voorkomen.