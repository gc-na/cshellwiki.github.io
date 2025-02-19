# [Linux] C Shell (csh) gunzip gebruik: Bestanden decomprimeren

## Overzicht
De `gunzip` opdracht wordt gebruikt om bestanden die zijn gecomprimeerd met gzip (GNU zip) te decomprimeren. Het herstelt de originele bestanden uit hun gecomprimeerde versie, waardoor ze weer toegankelijk zijn voor gebruik.

## Gebruik
De basis syntaxis van de `gunzip` opdracht is als volgt:

```csh
gunzip [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Schrijf de uitgepakte inhoud naar de standaarduitvoer in plaats van naar een bestand.
- `-f`: Forceer decomprimeren, zelfs als het doelbestand al bestaat.
- `-k`: Bewaar het originele gecomprimeerde bestand na decomprimeren.
- `-r`: Recursief decompressie uitvoeren in een directory.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `gunzip`:

1. Een enkel bestand decomprimeren:
   ```csh
   gunzip bestand.gz
   ```

2. De inhoud van een gecomprimeerd bestand naar de standaarduitvoer schrijven:
   ```csh
   gunzip -c bestand.gz
   ```

3. Een gecomprimeerd bestand behouden na decomprimeren:
   ```csh
   gunzip -k bestand.gz
   ```

4. Recursief decompressie uitvoeren in een directory:
   ```csh
   gunzip -r mapnaam/
   ```

## Tips
- Controleer altijd of er voldoende schijfruimte beschikbaar is voordat je grote bestanden decomprimeert.
- Gebruik de `-k` optie als je het originele bestand wilt behouden voor toekomstige referentie.
- Voor het decompressie van meerdere bestanden, kun je ze allemaal in één opdracht opgeven:
  ```csh
  gunzip bestand1.gz bestand2.gz
  ```