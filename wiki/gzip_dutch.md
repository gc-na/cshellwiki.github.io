# [Linux] Bash gzip gebruik: Bestanden comprimeren en decomprimeren

## Overzicht
De `gzip`-opdracht is een veelgebruikte tool in Unix-achtige systemen voor het comprimeren en decomprimeren van bestanden. Het vermindert de bestandsgrootte door gebruik te maken van de DEFLATE-compressiemethode, wat handig is voor het besparen van schijfruimte en het versnellen van bestandsoverdrachten.

## Gebruik
De basis syntaxis van de `gzip`-opdracht is als volgt:

```bash
gzip [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-d`, `--decompress`: Decomprimeert een bestand.
- `-k`, `--keep`: Houdt het originele bestand behouden na compressie.
- `-v`, `--verbose`: Toont gedetailleerde informatie over het compressieproces.
- `-r`, `--recursive`: Comprimeert bestanden in submappen.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `gzip`:

1. **Een bestand comprimeren**:
   ```bash
   gzip bestand.txt
   ```
   Dit zal `bestand.txt` comprimeren en het origineel verwijderen, resulterend in `bestand.txt.gz`.

2. **Een bestand decomprimeren**:
   ```bash
   gzip -d bestand.txt.gz
   ```
   Dit herstelt `bestand.txt` uit de gecomprimeerde versie.

3. **Een bestand comprimeren en het origineel behouden**:
   ```bash
   gzip -k bestand.txt
   ```
   Dit maakt een gecomprimeerd bestand `bestand.txt.gz`, terwijl `bestand.txt` behouden blijft.

4. **Alle bestanden in een map comprimeren**:
   ```bash
   gzip *.txt
   ```
   Dit comprimeert alle `.txt`-bestanden in de huidige map.

5. **Recursief bestanden in submappen comprimeren**:
   ```bash
   gzip -r mapnaam/
   ```
   Dit comprimeert alle bestanden in `mapnaam` en zijn submappen.

## Tips
- Gebruik de `-v` optie om te zien hoeveel ruimte je bespaart tijdens het compressieproces.
- Wees voorzichtig met het gebruik van `gzip` op grote bestanden, omdat het geheugen kan verbruiken.
- Overweeg om `tar` te gebruiken in combinatie met `gzip` voor het archiveren en comprimeren van meerdere bestanden in één stap. Bijvoorbeeld:
  ```bash
  tar -czf archief.tar.gz mapnaam/
  ```