# [Linux] Bash vmstat gebruik: Systeemstatistieken weergeven

## Overview
De `vmstat` (virtual memory statistics) opdracht geeft informatie weer over processen, geheugen, paginering, blokinvoer/uitvoer en CPU-activiteit. Het is een nuttig hulpmiddel voor systeembeheerders om de prestaties van een systeem te monitoren en te analyseren.

## Usage
De basis syntaxis van de `vmstat` opdracht is als volgt:

```bash
vmstat [opties] [argumenten]
```

## Common Options
Hier zijn enkele veelvoorkomende opties voor `vmstat`:

- `-a`: Toont alle geheugenstatistieken, inclusief vrij geheugen en buffers.
- `-m`: Toont informatie over de geheugenallocatie.
- `-s`: Toont een samenvatting van systeemstatistieken.
- `-t`: Toont tijdstempels bij de uitvoer.
- `[tijd]`: Geeft de interval in seconden aan voor herhaalde uitvoer.

## Common Examples

Hier zijn enkele praktische voorbeelden van het gebruik van `vmstat`:

1. **Basis gebruik zonder opties**:
   ```bash
   vmstat
   ```

2. **Statistieken elke 5 seconden weergeven**:
   ```bash
   vmstat 5
   ```

3. **Geheugenstatistieken weergeven met de `-a` optie**:
   ```bash
   vmstat -a
   ```

4. **Samenvatting van systeemstatistieken**:
   ```bash
   vmstat -s
   ```

5. **Statistieken met tijdstempels**:
   ```bash
   vmstat -t 5
   ```

## Tips
- Gebruik `vmstat` in combinatie met andere monitoringtools zoals `top` of `htop` voor een uitgebreidere analyse van systeembronnen.
- Monitor regelmatig om trends in systeemgebruik te identificeren en om potentiële problemen vroegtijdig te signaleren.
- Experimenteer met verschillende opties om de uitvoer aan te passen aan uw specifieke behoeften.