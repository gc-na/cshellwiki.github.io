# [Linux] C Shell (csh) gzip gebruik: Bestanden comprimeren

## Overzicht
De `gzip`-opdracht wordt gebruikt om bestanden te comprimeren met behulp van de GNU zip-compressiemethode. Het vermindert de bestandsgrootte, waardoor het efficiënter is om bestanden op te slaan en te verzenden.

## Gebruik
De basis syntaxis van de `gzip`-opdracht is als volgt:

```csh
gzip [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-d` : Decompressie van een bestand.
- `-k` : Houd het originele bestand intact na compressie.
- `-v` : Toon gedetailleerde informatie over het compressieproces.
- `-r` : Recursief compressie toepassen op alle bestanden in een directory.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `gzip`:

1. **Een enkel bestand comprimeren:**
   ```csh
   gzip bestand.txt
   ```

2. **Een bestand decompressie:**
   ```csh
   gzip -d bestand.txt.gz
   ```

3. **Een bestand comprimeren en het origineel behouden:**
   ```csh
   gzip -k bestand.txt
   ```

4. **Recursief compressie toepassen op alle .txt-bestanden in een directory:**
   ```csh
   gzip -r *.txt
   ```

5. **Gedetailleerde informatie over het compressieproces weergeven:**
   ```csh
   gzip -v bestand.txt
   ```

## Tips
- Gebruik de `-k` optie als je het originele bestand wilt behouden voor later gebruik.
- Controleer de bestandsgrootte na compressie met de `ls -lh` opdracht om te zien hoeveel ruimte je hebt bespaard.
- Voor het decompressieproces kun je ook de `gunzip` opdracht gebruiken, die een alias is voor `gzip -d`.