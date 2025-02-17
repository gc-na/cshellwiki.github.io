# [Linux] Bash lsblk Gebruik: Toont informatie over blokapparaten

## Overzicht
De `lsblk` (list block devices) opdracht in Bash wordt gebruikt om informatie weer te geven over de blokapparaten op een systeem. Dit omvat harde schijven, SSD's, USB-sticks en andere opslagmedia. De uitvoer toont een overzicht van de apparaten, hun partities en de bijbehorende schijfruimte.

## Gebruik
De basis syntaxis van de `lsblk` opdracht is als volgt:

```bash
lsblk [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a` of `--all`: Toont alle apparaten, inclusief lege apparaten.
- `-f` of `--fs`: Toont informatie over het bestandssysteem van de apparaten.
- `-l` of `--list`: Toont de uitvoer in een lijstvorm in plaats van een boomstructuur.
- `-o` of `--output`: Specificeert welke kolommen in de uitvoer moeten worden weergegeven.
- `-n` of `--noheadings`: Verbergt de koptekst in de uitvoer.

## Veelvoorkomende Voorbeelden

1. **Basisinformatie over blokapparaten weergeven:**
   ```bash
   lsblk
   ```

2. **Informatie over alle apparaten, inclusief lege apparaten:**
   ```bash
   lsblk -a
   ```

3. **Informatie over het bestandssysteem van de apparaten tonen:**
   ```bash
   lsblk -f
   ```

4. **Uitvoer in lijstvorm weergeven:**
   ```bash
   lsblk -l
   ```

5. **Specifieke kolommen weergeven, zoals naam en grootte:**
   ```bash
   lsblk -o NAME,SIZE
   ```

6. **Uitvoer zonder koptekst:**
   ```bash
   lsblk -n
   ```

## Tips
- Gebruik de `-f` optie om snel te controleren welk bestandssysteem op elk apparaat is geïnstalleerd.
- Combineer opties om de uitvoer aan te passen aan jouw behoeften, bijvoorbeeld `lsblk -f -o NAME,SIZE`.
- Vergeet niet dat `lsblk` alleen informatie toont over blokapparaten; gebruik `df` voor informatie over schijfruimte.