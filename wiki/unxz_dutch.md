# [Linux] Bash unxz gebruik: Bestanden decomprimeren

## Overzicht
De `unxz` opdracht wordt gebruikt om bestanden die zijn gecomprimeerd met het XZ-formaat te decomprimeren. Het is een eenvoudige en efficiënte manier om .xz-bestanden terug te brengen naar hun oorspronkelijke formaat.

## Gebruik
De basis syntaxis van de `unxz` opdracht is als volgt:

```bash
unxz [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-k`, `--keep`: Houd het originele gecomprimeerde bestand na decomprimeren.
- `-f`, `--force`: Dwingt de decompressie, zelfs als het doelbestand al bestaat.
- `-v`, `--verbose`: Toon gedetailleerde informatie tijdens het decomprimeren.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `unxz`:

1. **Een enkel .xz-bestand decomprimeren:**
   ```bash
   unxz bestand.xz
   ```

2. **Een .xz-bestand decomprimeren en het originele bestand behouden:**
   ```bash
   unxz -k bestand.xz
   ```

3. **Een .xz-bestand forceren om te decomprimeren, zelfs als het doelbestand al bestaat:**
   ```bash
   unxz -f bestand.xz
   ```

4. **Decompressie met gedetailleerde uitvoer:**
   ```bash
   unxz -v bestand.xz
   ```

## Tips
- Gebruik de `-k` optie als je het originele bestand wilt behouden voor toekomstige referentie.
- Controleer altijd of er voldoende schijfruimte is voordat je grote bestanden decomprimeert.
- Combineer `unxz` met andere commando's, zoals `tar`, om gecomprimeerde archieven efficiënt te beheren.