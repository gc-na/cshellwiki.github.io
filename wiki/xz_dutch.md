# [Linux] Bash xz gebruik: Gegevenscompressie en decompressie

## Overzicht
De `xz` opdracht is een krachtige tool voor gegevenscompressie die gebruikmaakt van het LZMA-algoritme. Het wordt vaak gebruikt om bestanden te verkleinen, waardoor opslagruimte wordt bespaard en de overdrachtstijd van bestanden wordt versneld.

## Gebruik
De basis syntaxis van de `xz` opdracht is als volgt:

```bash
xz [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-d`, `--decompress`: Decomprimeert een bestand.
- `-k`, `--keep`: Houdt het originele bestand na compressie of decompressie.
- `-f`, `--force`: Dwingt de opdracht om bestaande bestanden te overschrijven.
- `-9`: Stelt het compressieniveau in op maximaal (9), wat resulteert in de kleinste bestandsgrootte, maar meer tijd kost.
- `-t`, `--test`: Test een gecomprimeerd bestand zonder het daadwerkelijk te decomprimeren.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `xz` opdracht:

1. **Bestand comprimeren:**
   ```bash
   xz bestand.txt
   ```
   Dit comprimeert `bestand.txt` en maakt `bestand.txt.xz`.

2. **Bestand decomprimeren:**
   ```bash
   xz -d bestand.txt.xz
   ```
   Dit decomprimeert `bestand.txt.xz` terug naar `bestand.txt`.

3. **Bestand comprimeren en origineel behouden:**
   ```bash
   xz -k bestand.txt
   ```
   Dit maakt een gecomprimeerd bestand `bestand.txt.xz` en behoudt het originele `bestand.txt`.

4. **Bestand testen zonder decompressie:**
   ```bash
   xz -t bestand.txt.xz
   ```
   Dit test of `bestand.txt.xz` correct is gecomprimeerd.

## Tips
- Gebruik de optie `-9` voor maximale compressie als opslagruimte een prioriteit is, maar wees bewust dat dit meer tijd kost.
- Combineer `xz` met andere commando's zoals `tar` voor het archiveren en comprimeren van meerdere bestanden in één stap.
- Controleer regelmatig de integriteit van gecomprimeerde bestanden met de `-t` optie om ervoor te zorgen dat ze niet beschadigd zijn.