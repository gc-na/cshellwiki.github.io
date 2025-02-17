# [Linux] Bash clear gebruik: Verwijder de terminalinhoud

## Overview
De `clear` opdracht in Bash wordt gebruikt om de terminalinhoud te wissen. Dit is handig om een schone werkruimte te creëren, vooral wanneer de terminal vol is met tekst en je een frisse start wilt maken.

## Usage
De basis syntaxis van de `clear` opdracht is als volgt:

```bash
clear [opties]
```

## Common Options
Hier zijn enkele veelvoorkomende opties voor de `clear` opdracht:

- `-x`: Verwijdert de terminalinhoud en herstelt de cursor naar de bovenkant van het scherm.
- `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `--version`: Geeft de versie-informatie van de `clear` opdracht weer.

## Common Examples
Hier zijn enkele praktische voorbeelden van het gebruik van de `clear` opdracht:

1. Gewoon de terminal wissen:
   ```bash
   clear
   ```

2. De terminal wissen en de cursor naar de bovenkant van het scherm verplaatsen:
   ```bash
   clear -x
   ```

3. Hulpinformatie opvragen:
   ```bash
   clear --help
   ```

4. Versie-informatie opvragen:
   ```bash
   clear --version
   ```

## Tips
- Gebruik `clear` regelmatig om je terminal overzichtelijk te houden, vooral tijdens lange sessies.
- Combineer `clear` met andere opdrachten in scripts om de uitvoer te organiseren.
- Vergeet niet dat `clear` alleen de zichtbare terminalinhoud verwijdert; het heeft geen invloed op de geschiedenis van de terminal.