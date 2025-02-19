# [Linux] C Shell (csh) xz gebruik: Gegevenscompressie en decompressie

## Overzicht
De `xz` opdracht is een krachtige tool voor het comprimeren en decomprimeren van bestanden. Het maakt gebruik van het LZMA-algoritme, dat zorgt voor hoge compressieverhoudingen en efficiëntie.

## Gebruik
De basis syntaxis van de `xz` opdracht is als volgt:

```bash
xz [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-d`, `--decompress`: Decomprimeer een bestand.
- `-k`, `--keep`: Houd het originele bestand na compressie of decompressie.
- `-v`, `--verbose`: Toon gedetailleerde informatie tijdens de compressie of decompressie.
- `-9`: Gebruik de hoogste compressie (langzamer, maar kleinere bestanden).

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `xz` opdracht:

### Bestanden comprimeren
Om een bestand genaamd `voorbeeld.txt` te comprimeren, gebruik je:

```bash
xz voorbeeld.txt
```

### Bestanden decomprimeren
Om een gecomprimeerd bestand genaamd `voorbeeld.txt.xz` te decomprimeren, gebruik je:

```bash
xz -d voorbeeld.txt.xz
```

### Origineel bestand behouden
Als je het originele bestand wilt behouden tijdens het comprimeren, gebruik je:

```bash
xz -k voorbeeld.txt
```

### Gedetailleerde uitvoer
Om gedetailleerde informatie te krijgen tijdens het compressieproces, gebruik je:

```bash
xz -v voorbeeld.txt
```

## Tips
- Gebruik de `-9` optie voor de beste compressie als de bestandsgrootte cruciaal is, maar wees je bewust van de langere verwerkingstijd.
- Controleer altijd de beschikbare schijfruimte voordat je grote bestanden comprimeert, vooral als je de originele bestanden wilt behouden.
- Combineer `xz` met andere commando's zoals `tar` voor het archiveren en comprimeren van meerdere bestanden in één stap.