# [Linux] Bash cksum gebruik: bereken controlegetallen van bestanden

## Overzicht
De `cksum`-opdracht in Bash wordt gebruikt om een controlegetal (checksum) en de bestandsgrootte van een bestand te berekenen. Dit kan nuttig zijn voor het verifiëren van de integriteit van bestanden door te controleren of ze niet zijn gewijzigd.

## Gebruik
De basis syntaxis van de `cksum`-opdracht is als volgt:

```bash
cksum [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a, --algorithm=ALG`: Specificeert het algoritme dat gebruikt moet worden voor het berekenen van de checksum.
- `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `--version`: Toont de versie-informatie van de `cksum`-opdracht.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `cksum`-opdracht:

1. **Bereken de checksum van een bestand:**
   ```bash
   cksum bestand.txt
   ```

2. **Bereken de checksum van meerdere bestanden:**
   ```bash
   cksum bestand1.txt bestand2.txt
   ```

3. **Gebruik de `--help` optie om meer informatie te krijgen:**
   ```bash
   cksum --help
   ```

4. **Bereken de checksum van een bestand en sla de uitvoer op in een tekstbestand:**
   ```bash
   cksum bestand.txt > checksum.txt
   ```

## Tips
- Gebruik `cksum` in combinatie met andere opdrachten zoals `diff` om bestanden te vergelijken op basis van hun checksum.
- Bewaar de checksum van belangrijke bestanden om later de integriteit te kunnen verifiëren.
- Houd er rekening mee dat de `cksum`-opdracht een andere checksum genereert dan andere tools zoals `md5sum` of `sha256sum`, dus gebruik de juiste tool voor jouw behoeften.