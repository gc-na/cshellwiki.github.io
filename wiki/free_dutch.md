# [Linux] C Shell (csh) free gebruik: Toont geheugeninformatie

## Overzicht
De `free` opdracht in C Shell (csh) wordt gebruikt om informatie over het geheugen van het systeem weer te geven. Het toont de totale hoeveelheid geheugen, het gebruikte geheugen, het vrije geheugen en de buffers/caches die door het systeem worden gebruikt.

## Gebruik
De basis syntaxis van de `free` opdracht is als volgt:

```csh
free [opties]
```

## Veelvoorkomende Opties
- `-h`: Toont de geheugeninformatie in een leesbaar formaat (bijvoorbeeld in MB of GB).
- `-m`: Toont de geheugeninformatie in megabytes.
- `-g`: Toont de geheugeninformatie in gigabytes.
- `-s [interval]`: Herhaalt de uitvoer elke [interval] seconden.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `free` opdracht:

1. Basis geheugeninformatie weergeven:
   ```csh
   free
   ```

2. Geheugeninformatie in een leesbaar formaat weergeven:
   ```csh
   free -h
   ```

3. Geheugeninformatie in megabytes weergeven:
   ```csh
   free -m
   ```

4. Geheugeninformatie in gigabytes weergeven:
   ```csh
   free -g
   ```

5. Geheugeninformatie elke 5 seconden vernieuwen:
   ```csh
   free -s 5
   ```

## Tips
- Gebruik de `-h` optie voor een gemakkelijk leesbare uitvoer, vooral als je met grote hoeveelheden geheugen werkt.
- Combineer de `-s` optie met andere opties om continu de geheugenstatus te monitoren.
- Controleer regelmatig het geheugen om te zien of er voldoende middelen beschikbaar zijn voor je toepassingen.