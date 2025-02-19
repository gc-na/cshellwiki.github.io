# [Linux] C Shell (csh) mpstat gebruik: Toont CPU-statistieken

## Overzicht
De `mpstat` opdracht is een hulpmiddel dat informatie geeft over de CPU-activiteit op een systeem. Het toont statistieken per processor, wat nuttig is voor het analyseren van de prestaties en het identificeren van knelpunten.

## Gebruik
De basis syntaxis van de `mpstat` opdracht is als volgt:

```csh
mpstat [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-P ALL`: Toon statistieken voor alle CPU's.
- `-u`: Toon alleen de gebruiksstatistieken van de CPU.
- `-h`: Toon de helpinformatie voor de opdracht.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `mpstat`:

1. Toon CPU-statistieken voor alle CPU's:
    ```csh
    mpstat -P ALL
    ```

2. Toon alleen de gebruiksstatistieken van de CPU:
    ```csh
    mpstat -u
    ```

3. Toon CPU-statistieken met een interval van 5 seconden:
    ```csh
    mpstat 5
    ```

4. Toon CPU-statistieken voor een specifieke CPU (bijvoorbeeld CPU 0):
    ```csh
    mpstat -P 0
    ```

## Tips
- Gebruik `mpstat` in combinatie met andere monitoringtools voor een uitgebreidere analyse van systeemprestaties.
- Regelmatig gebruik van `mpstat` kan helpen bij het identificeren van trends in CPU-gebruik over de tijd.
- Vergeet niet om de juiste opties te gebruiken om alleen de informatie te krijgen die je nodig hebt.