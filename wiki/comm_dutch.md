# [Linux] Bash comm gebruik: Vergelijk twee gesorteerde bestanden

## Overzicht
De `comm`-opdracht in Bash wordt gebruikt om de overeenkomsten en verschillen tussen twee gesorteerde bestanden te vergelijken. Het geeft de inhoud van beide bestanden weer, waarbij het resultaat in drie kolommen wordt gepresenteerd: unieke regels in het eerste bestand, unieke regels in het tweede bestand en regels die in beide bestanden voorkomen.

## Gebruik
De basis syntaxis van de `comm`-opdracht is als volgt:

```bash
comm [opties] [bestand1] [bestand2]
```

## Veelvoorkomende Opties
- `-1`: Onderdruk de eerste kolom (unieke regels in het eerste bestand).
- `-2`: Onderdruk de tweede kolom (unieke regels in het tweede bestand).
- `-3`: Onderdruk de derde kolom (gemeenschappelijke regels).
- `-i`: Negeer hoofdlettergebruik bij de vergelijking.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Basisgebruik
Vergelijk twee gesorteerde bestanden `file1.txt` en `file2.txt`:

```bash
comm file1.txt file2.txt
```

### Voorbeeld 2: Alleen gemeenschappelijke regels tonen
Toon alleen de regels die in beide bestanden voorkomen:

```bash
comm -12 file1.txt file2.txt
```

### Voorbeeld 3: Unieke regels in het tweede bestand
Toon alleen de regels die uniek zijn voor `file2.txt`:

```bash
comm -13 file1.txt file2.txt
```

### Voorbeeld 4: Hoofdlettergevoeligheid negeren
Vergelijk twee bestanden zonder rekening te houden met hoofdletters:

```bash
comm -i file1.txt file2.txt
```

## Tips
- Zorg ervoor dat de bestanden gesorteerd zijn voordat je `comm` gebruikt, anders krijg je onverwachte resultaten. Gebruik de `sort`-opdracht om bestanden te sorteren.
- Combineer `comm` met andere opdrachten zoals `sort` en `uniq` voor geavanceerdere tekstverwerking.
- Gebruik de opties om alleen de informatie te tonen die je nodig hebt, wat de uitvoer overzichtelijker maakt.