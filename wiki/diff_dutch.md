# [Linux] Bash diff gebruik: Vergelijk bestanden en mappen

## Overzicht
Het `diff`-commando wordt gebruikt om de verschillen tussen twee bestanden of mappen te vergelijken. Het toont de regels die zijn toegevoegd, verwijderd of gewijzigd, waardoor het een handig hulpmiddel is voor programmeurs en gebruikers die wijzigingen in tekstbestanden willen analyseren.

## Gebruik
De basis syntaxis van het `diff`-commando is als volgt:

```bash
diff [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-u`: Toon de verschillen in een "unified" formaat, wat het gemakkelijker maakt om wijzigingen te begrijpen.
- `-i`: Negeer hoofdlettergebruik bij de vergelijking.
- `-w`: Negeer spaties en tabs in de vergelijking.
- `-r`: Vergelijk mappen recursief.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Basis vergelijking van twee bestanden
```bash
diff bestand1.txt bestand2.txt
```

### Voorbeeld 2: Gebruik van de unified optie
```bash
diff -u bestand1.txt bestand2.txt
```

### Voorbeeld 3: Vergelijking met genegeerde hoofdletters
```bash
diff -i bestand1.txt bestand2.txt
```

### Voorbeeld 4: Vergelijking van twee mappen
```bash
diff -r map1/ map2/
```

## Tips
- Gebruik de `-u` optie voor een duidelijker overzicht van de wijzigingen.
- Combineer opties voor meer specifieke vergelijkingen, zoals `diff -u -w bestand1.txt bestand2.txt`.
- Sla de uitvoer op in een bestand met `diff bestand1.txt bestand2.txt > verschillen.txt` om later te kunnen analyseren.