# [Linux] C Shell (csh) touch gebruik: Bestanden maken of bijwerken

## Overzicht
De `touch`-opdracht in C Shell (csh) wordt gebruikt om de tijdstempels van bestanden bij te werken of om nieuwe, lege bestanden te maken als ze nog niet bestaan.

## Gebruik
De basis syntaxis van de `touch`-opdracht is als volgt:

```csh
touch [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a`: Werk alleen de toegangstijd bij.
- `-m`: Werk alleen de wijzigingstijd bij.
- `-c`: Maak geen nieuwe bestanden aan; alleen bestaande bestanden bijwerken.
- `-t`: Stel een specifieke tijdstempel in (in het formaat [[CC]YY]MMDDhhmm[.ss]).

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `touch`:

1. Maak een nieuw, leeg bestand aan:
   ```csh
   touch nieuw_bestand.txt
   ```

2. Werk de tijdstempel van een bestaand bestand bij:
   ```csh
   touch bestaand_bestand.txt
   ```

3. Werk alleen de toegangstijd bij:
   ```csh
   touch -a bestaand_bestand.txt
   ```

4. Stel een specifieke tijdstempel in voor een bestand:
   ```csh
   touch -t 202301011200.00 specifiek_bestand.txt
   ```

5. Maak geen nieuwe bestanden aan, maar werk alleen bestaande bestanden bij:
   ```csh
   touch -c niet_bestaand_bestand.txt
   ```

## Tips
- Gebruik `touch` om snel de tijdstempels van meerdere bestanden bij te werken door ze allemaal in één opdracht op te sommen.
- Controleer altijd of je de juiste opties gebruikt, vooral bij het instellen van specifieke tijdstempels, om ongewenste wijzigingen te voorkomen.
- Combineer `touch` met andere opdrachten in scripts om efficiënter met bestanden te werken.