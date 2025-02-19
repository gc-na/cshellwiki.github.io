# [Linux] C Shell (csh) cp gebruik: Bestanden kopiëren

## Overzicht
De `cp`-opdracht wordt gebruikt om bestanden en directories te kopiëren in de C Shell. Het is een essentiële tool voor het beheren van bestanden op een systeem.

## Gebruik
De basis syntaxis van de `cp`-opdracht is als volgt:

```
cp [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-i`: Vraagt om bevestiging voordat een bestaand bestand wordt overschreven.
- `-r`: Kopieert directories en hun inhoud recursief.
- `-u`: Kopieert alleen als het bronbestand nieuwer is dan het doelbestand of als het doelbestand niet bestaat.
- `-v`: Toont de voortgang van de kopieeractie (verbose).

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `cp`-opdracht:

1. **Een enkel bestand kopiëren:**
   ```csh
   cp bestand.txt kopie_bestand.txt
   ```

2. **Een directory en zijn inhoud kopiëren:**
   ```csh
   cp -r mijn_map/ kopie_mijn_map/
   ```

3. **Een bestand kopiëren met bevestiging:**
   ```csh
   cp -i bestand.txt kopie_bestand.txt
   ```

4. **Bestanden kopiëren met verbose output:**
   ```csh
   cp -v bestand1.txt bestand2.txt
   ```

5. **Een bestand kopiëren als het bronbestand nieuwer is:**
   ```csh
   cp -u bestand.txt kopie_bestand.txt
   ```

## Tips
- Gebruik de `-i` optie om per ongeluk overschrijven van bestanden te voorkomen.
- Bij het kopiëren van directories, vergeet niet de `-r` optie te gebruiken om ervoor te zorgen dat alle inhoud wordt gekopieerd.
- Controleer altijd de bestandsrechten na het kopiëren om ervoor te zorgen dat ze correct zijn ingesteld.