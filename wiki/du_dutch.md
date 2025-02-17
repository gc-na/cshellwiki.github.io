# [Linux] Bash du gebruik: Toon schijfruimtegebruik

## Overzicht
De `du` (disk usage) opdracht in Bash wordt gebruikt om de schijfruimte te tonen die door bestanden en directories wordt gebruikt. Het is een nuttige tool voor het analyseren van schijfruimte en het identificeren van grote bestanden of mappen.

## Gebruik
De basis syntaxis van de `du` opdracht is als volgt:

```bash
du [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`: Toont de schijfruimte in een leesbaar formaat (bijv. K, M, G).
- `-s`: Geeft alleen de totale grootte van de opgegeven directory weer.
- `-a`: Toont de grootte van alle bestanden, niet alleen directories.
- `-c`: Geeft een totaal weer van de schijfruimte voor alle opgegeven argumenten.
- `--max-depth=N`: Beperk de diepte van de directorystructuur die wordt weergegeven tot N niveaus.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `du` opdracht:

1. Toon de schijfruimte van de huidige directory in een leesbaar formaat:
   ```bash
   du -h
   ```

2. Toon alleen de totale grootte van een specifieke directory:
   ```bash
   du -sh /pad/naar/directory
   ```

3. Toon de schijfruimte van alle bestanden en directories in de huidige directory:
   ```bash
   du -ah
   ```

4. Toon de schijfruimte van een directory met een maximum diepte van 1:
   ```bash
   du --max-depth=1 -h /pad/naar/directory
   ```

5. Toon de totale schijfruimte van meerdere directories:
   ```bash
   du -ch /pad/naar/directory1 /pad/naar/directory2
   ```

## Tips
- Gebruik de `-h` optie om de uitvoer gemakkelijker te maken om te lezen, vooral bij grote bestanden.
- Combineer `du` met andere commando's zoals `sort` om de grootste bestanden of directories bovenaan te krijgen:
  ```bash
  du -ah | sort -rh | head -n 10
  ```
- Vergeet niet dat `du` de schijfruimte toont zoals deze wordt gebruikt op de schijf, wat kan verschillen van de bestandsgrootte in het bestandssysteem.