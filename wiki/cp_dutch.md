# [Linux] Bash cp gebruik: Bestanden kopiëren

## Overzicht
De `cp`-opdracht in Bash wordt gebruikt om bestanden en mappen te kopiëren van de ene locatie naar de andere. Het is een essentieel hulpmiddel voor bestandbeheer in een Linux-omgeving.

## Gebruik
De basis syntaxis van de `cp`-opdracht is als volgt:

```bash
cp [opties] [bronnen] [doel]
```

## Veelvoorkomende Opties
- `-r`: Kopieert mappen en hun inhoud recursief.
- `-i`: Vraagt om bevestiging voordat bestaande bestanden worden overschreven.
- `-u`: Kopieert alleen bestanden die nieuwere versies hebben dan de bestanden in de doelmap.
- `-v`: Geeft gedetailleerde informatie over wat er wordt gekopieerd.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `cp`-opdracht:

1. **Een bestand kopiëren naar een andere locatie:**
   ```bash
   cp bestand.txt /pad/naar/doelmap/
   ```

2. **Een map en zijn inhoud kopiëren:**
   ```bash
   cp -r mapnaam /pad/naar/doelmap/
   ```

3. **Een bestand kopiëren met bevestiging:**
   ```bash
   cp -i bestand.txt /pad/naar/doelmap/
   ```

4. **Alleen nieuwere bestanden kopiëren:**
   ```bash
   cp -u bestand.txt /pad/naar/doelmap/
   ```

5. **Gedetailleerde uitvoer tijdens het kopiëren:**
   ```bash
   cp -v bestand.txt /pad/naar/doelmap/
   ```

## Tips
- Gebruik de `-i` optie om per ongeluk overschrijven van bestanden te voorkomen.
- Bij het kopiëren van grote mappen, overweeg om de `-v` optie te gebruiken om te zien wat er gebeurt.
- Controleer altijd de doelmap na het kopiëren om er zeker van te zijn dat alles correct is overgezet.