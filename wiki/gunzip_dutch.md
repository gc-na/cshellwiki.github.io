# [Linux] Bash gunzip gebruik: Bestanden decomprimeren

## Overzicht
De `gunzip` opdracht wordt gebruikt om bestanden die zijn gecomprimeerd met gzip (GNU zip) te decomprimeren. Het herstelt de originele bestanden uit hun gecomprimeerde versie, waardoor ze weer toegankelijk zijn voor gebruik.

## Gebruik
De basis syntaxis van de `gunzip` opdracht is als volgt:

```bash
gunzip [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Schrijft de uitgepakte gegevens naar standaarduitvoer in plaats van naar een bestand.
- `-f`: Dwingt het overschrijven van bestaande bestanden zonder bevestiging.
- `-k`: Houdt het originele gecomprimeerde bestand na decompressie.
- `-r`: Decomprimeert bestanden in een directory en zijn subdirectories.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `gunzip`:

1. **Een enkel bestand decomprimeren:**
   ```bash
   gunzip bestand.gz
   ```

2. **Een bestand decomprimeren en het originele bestand behouden:**
   ```bash
   gunzip -k bestand.gz
   ```

3. **Decomprimeren van meerdere bestanden:**
   ```bash
   gunzip bestand1.gz bestand2.gz
   ```

4. **Decomprimeren en de uitvoer naar een bestand schrijven:**
   ```bash
   gunzip -c bestand.gz > uitvoer.txt
   ```

5. **Decomprimeren van alle .gz bestanden in een directory:**
   ```bash
   gunzip *.gz
   ```

## Tips
- Controleer altijd of je voldoende schijfruimte hebt voordat je bestanden decomprimeert, omdat de originele bestanden mogelijk veel ruimte in beslag nemen.
- Gebruik de `-v` optie voor een gedetailleerde uitvoer van het decompressieproces, wat handig kan zijn voor foutopsporing.
- Wees voorzichtig met de `-f` optie, omdat deze bestaande bestanden zonder waarschuwing kan overschrijven.