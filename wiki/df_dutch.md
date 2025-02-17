# [Linux] Bash df gebruik: Toont schijfruimte-informatie

## Overzicht
De `df` (disk free) opdracht in Bash wordt gebruikt om informatie weer te geven over de beschikbare en gebruikte schijfruimte op bestandssystemen. Het helpt gebruikers om een overzicht te krijgen van de schijfruimte op hun systeem.

## Gebruik
De basis syntaxis van de `df` opdracht is als volgt:

```bash
df [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`: Toont de schijfruimte in een leesbaar formaat (bijvoorbeeld in KB, MB of GB).
- `-T`: Toont het type van het bestandssysteem.
- `-a`: Toont ook de bestandssystemen die geen ruimte hebben.
- `-i`: Toont informatie over inodes in plaats van schijfruimte.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `df` opdracht:

1. Toon schijfruimte in een leesbaar formaat:
   ```bash
   df -h
   ```

2. Toon schijfruimte met bestandssysteemtypes:
   ```bash
   df -T
   ```

3. Toon alle bestandssystemen, inclusief die zonder ruimte:
   ```bash
   df -a
   ```

4. Toon informatie over inodes:
   ```bash
   df -i
   ```

## Tips
- Gebruik de `-h` optie voor een beter leesbare weergave van schijfruimte, vooral als je met grote hoeveelheden gegevens werkt.
- Combineer opties voor meer gedetailleerde informatie, bijvoorbeeld `df -hT` om zowel de schijfruimte als het type bestandssysteem te zien.
- Controleer regelmatig je schijfruimte om te voorkomen dat je schijf vol raakt, wat kan leiden tot systeemproblemen.