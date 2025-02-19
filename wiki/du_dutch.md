# [Linux] C Shell (csh) du gebruik: Toon schijfruimtegebruik

## Overzicht
De `du` (disk usage) opdracht in C Shell wordt gebruikt om de schijfruimte die door bestanden en directories wordt gebruikt te rapporteren. Het geeft een overzicht van de grootte van bestanden en mappen, wat nuttig is voor het beheren van schijfruimte.

## Gebruik
De basis syntaxis van de `du` opdracht is als volgt:

```csh
du [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`: Toont de grootte in een leesbaar formaat (bijv. KB, MB).
- `-s`: Geeft alleen de totale grootte van de opgegeven directory weer.
- `-a`: Toont de grootte van alle bestanden, niet alleen directories.
- `-c`: Geeft een totaal weer aan het einde van de uitvoer.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `du` opdracht:

1. Toon de schijfruimte van de huidige directory in een leesbaar formaat:
    ```csh
    du -h
    ```

2. Toon alleen de totale grootte van een specifieke directory:
    ```csh
    du -sh /pad/naar/directory
    ```

3. Toon de grootte van alle bestanden en directories in de huidige directory:
    ```csh
    du -ah
    ```

4. Toon de grootte van een directory en geef een totaal weer:
    ```csh
    du -ch /pad/naar/directory
    ```

## Tips
- Gebruik de `-h` optie voor een beter leesbare uitvoer, vooral als je met grote bestanden werkt.
- Combineer de `-s` optie met specifieke paden om snel de totale grootte van belangrijke directories te controleren.
- Houd rekening met de schijfruimte van tijdelijke bestanden en caches, deze kunnen soms veel ruimte innemen.