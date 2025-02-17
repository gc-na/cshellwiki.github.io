# [Linux] Bash stat gebruik: Toon bestandseigenschappen

## Overzicht
De `stat`-opdracht in Bash wordt gebruikt om gedetailleerde informatie over bestanden en directories weer te geven. Het toont metadata zoals de bestandsgrootte, de laatste wijzigingsdatum, en de bestandspermissies.

## Gebruik
De basis syntaxis van de `stat`-opdracht is als volgt:

```bash
stat [opties] [argumenten]
```

## Veelvoorkomende opties
- `-c` : Specificeer een opmaak voor de uitvoer.
- `--format` : Een alternatieve manier om de uitvoer op te maken.
- `-f` : Toon informatie over het bestandssysteem in plaats van het bestand zelf.
- `-L` : Volg symbolische links en toon informatie over het doelbestand.

## Veelvoorkomende voorbeelden

### Basisinformatie over een bestand
Om basisinformatie over een bestand te krijgen, gebruik je:

```bash
stat bestand.txt
```

### Specifieke opmaak van de uitvoer
Als je alleen de bestandsgrootte wilt weergeven, kun je de `-c` optie gebruiken:

```bash
stat -c %s bestand.txt
```

### Informatie over een directory
Om informatie over een directory te krijgen, gebruik je:

```bash
stat /pad/naar/directory
```

### Informatie over een symbolische link
Om informatie over het doel van een symbolische link te krijgen, gebruik je de `-L` optie:

```bash
stat -L symlink.txt
```

## Tips
- Gebruik de `-c` optie om de uitvoer aan te passen aan jouw behoeften, wat handig kan zijn voor scripts.
- Combineer `stat` met andere commando's zoals `grep` om specifieke informatie te filteren.
- Vergeet niet dat `stat` ook werkt met directories, niet alleen met bestanden, wat handig kan zijn voor systeembeheer.