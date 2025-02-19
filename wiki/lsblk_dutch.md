# [Linux] C Shell (csh) lsblk gebruik: Toont informatie over blokapparaten

## Overzicht
De `lsblk`-opdracht wordt gebruikt om informatie weer te geven over blokapparaten op een Linux-systeem. Dit omvat harde schijven, SSD's, USB-sticks en andere opslagmedia. Het biedt een overzicht van de schijfstructuur, inclusief partities en hun mount-punten.

## Gebruik
De basis syntaxis van de `lsblk`-opdracht is als volgt:

```bash
lsblk [opties] [argumenten]
```

## Veelvoorkomende opties
- `-a`, `--all`: Toont ook lege apparaten.
- `-f`, `--fs`: Toont bestandsysteeminformatie.
- `-l`, `--list`: Toont de uitvoer in een lijstvorm in plaats van een boomstructuur.
- `-o`, `--output`: Specificeert welke kolommen moeten worden weergegeven.
- `-n`, `--noheadings`: Verbergt de koptekst in de uitvoer.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `lsblk`:

1. **Basisinformatie over blokapparaten weergeven:**
   ```bash
   lsblk
   ```

2. **Toon ook lege apparaten:**
   ```bash
   lsblk -a
   ```

3. **Toon bestandsysteeminformatie:**
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

## Tips
- Gebruik de `-n` optie om de uitvoer te vereenvoudigen zonder kopteksten, vooral handig voor scripting.
- Combineer opties zoals `-f` en `-o` om gedetailleerde informatie over besturingssystemen en schijven te verkrijgen.
- Controleer regelmatig de status van je schijven met `lsblk` om een overzicht te behouden van je opslagapparaten en hun partities.