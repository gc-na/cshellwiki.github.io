# [Linux] C Shell (csh) nl: nummeren van regels in een bestand

## Overview
De `nl` opdracht in C Shell (csh) wordt gebruikt om de regels van een tekstbestand te nummeren. Dit is handig voor het maken van overzichtelijke documenten of het analyseren van codebestanden.

## Usage
De basis syntaxis van de `nl` opdracht is als volgt:

```csh
nl [opties] [argumenten]
```

## Common Options
Hier zijn enkele veelvoorkomende opties voor de `nl` opdracht:

- `-b` : Bepaalt hoe regels worden genummerd (bijvoorbeeld alleen niet-lege regels).
- `-f` : Geeft aan dat een bepaalde regel als een nieuwe pagina moet worden behandeld.
- `-n` : Bepaalt het nummerformaat (bijvoorbeeld links of rechts uitgelijnd).
- `-w` : Stelt de breedte in van het nummer.

## Common Examples
Hier zijn enkele praktische voorbeelden van het gebruik van de `nl` opdracht:

1. Nummeren van alle regels in een bestand:
   ```csh
   nl bestand.txt
   ```

2. Nummeren van alleen niet-lege regels:
   ```csh
   nl -b a bestand.txt
   ```

3. Nummeren met een specifieke breedte:
   ```csh
   nl -w 4 bestand.txt
   ```

4. Nummeren en de uitvoer naar een nieuw bestand schrijven:
   ```csh
   nl bestand.txt > genummerd_bestand.txt
   ```

## Tips
- Gebruik de optie `-b` om te bepalen welke regels genummerd moeten worden, zodat je alleen relevante informatie krijgt.
- Experimenteer met de `-n` optie om te zien welk nummerformaat het beste werkt voor jouw document.
- Combineer `nl` met andere opdrachten, zoals `grep`, om specifieke regels te nummeren in een gefilterde uitvoer.