# [Linux] Bash basename gebruik: Haal de bestandsnaam uit een pad

## Overzicht
De `basename`-opdracht in Bash wordt gebruikt om de naam van een bestand of directory uit een volledig pad te extraheren. Dit kan handig zijn wanneer je alleen de naam wilt zonder het pad.

## Gebruik
De basis syntaxis van de `basename`-opdracht is als volgt:

```bash
basename [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a`: Verwerkt meerdere argumenten en retourneert de basisnamen voor elk.
- `-s`: Verwijdert een specifieke suffix van de bestandsnaam.

## Veelvoorkomende Voorbeelden

1. **Basisnaam van een enkel bestand**
   ```bash
   basename /pad/naar/bestand.txt
   ```
   Dit retourneert:
   ```
   bestand.txt
   ```

2. **Basisnaam met een suffix verwijderen**
   ```bash
   basename /pad/naar/bestand.txt .txt
   ```
   Dit retourneert:
   ```
   bestand
   ```

3. **Meerdere bestanden verwerken**
   ```bash
   basename -a /pad/naar/bestand1.txt /pad/naar/bestand2.txt
   ```
   Dit retourneert:
   ```
   bestand1.txt
   bestand2.txt
   ```

4. **Basisnaam van een directory**
   ```bash
   basename /pad/naar/directory/
   ```
   Dit retourneert:
   ```
   directory
   ```

## Tips
- Gebruik `basename` in scripts om bestandsnamen dynamisch te extraheren.
- Combineer `basename` met andere commando's zoals `find` voor geavanceerdere bestandsverwerking.
- Vergeet niet om de juiste suffix op te geven als je deze wilt verwijderen, om onverwachte resultaten te voorkomen.