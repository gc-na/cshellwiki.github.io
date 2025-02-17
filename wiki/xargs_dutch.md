# [Linux] Bash xargs gebruik: Verwerkt argumenten van standaardinvoer

## Overzicht
Het `xargs`-commando in Bash wordt gebruikt om argumenten van standaardinvoer om te zetten in opdrachten die aan andere commando's kunnen worden doorgegeven. Dit is bijzonder nuttig wanneer je een lijst van items wilt verwerken die door een ander commando zijn geproduceerd, zoals `find` of `grep`.

## Gebruik
De basis syntaxis van het `xargs`-commando is als volgt:

```bash
xargs [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n N`: Geef maximaal N argumenten door aan het volgende commando.
- `-d DELIM`: Gebruik DELIM als scheidingsteken in plaats van spaties of nieuwe regels.
- `-0`: Verwerkt invoer die is gescheiden door null-terminators, handig voor bestandsnamen met spaties.
- `-p`: Vraag bevestiging voordat een opdracht wordt uitgevoerd.
- `-I {}`: Vervang `{}` door de invoer in de opgegeven opdracht.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Bestanden verwijderen
Gebruik `find` om bestanden te vinden en `xargs` om ze te verwijderen.

```bash
find . -name "*.tmp" | xargs rm
```

### Voorbeeld 2: Bestanden kopiëren
Kopieer bestanden naar een andere map met behulp van `find` en `xargs`.

```bash
find . -name "*.jpg" | xargs -I {} cp {} /pad/naar/doelmap/
```

### Voorbeeld 3: Aantal regels tellen
Tel het aantal regels in meerdere tekstbestanden.

```bash
ls *.txt | xargs wc -l
```

### Voorbeeld 4: Bestanden met spaties
Gebruik `-0` om bestanden met spaties correct te verwerken.

```bash
find . -name "*.pdf" -print0 | xargs -0 cp -t /pad/naar/doelmap/
```

## Tips
- Gebruik `-n` om het aantal argumenten dat naar het volgende commando wordt doorgestuurd te beperken, wat handig kan zijn voor commando's die niet goed werken met een groot aantal argumenten.
- Combineer `xargs` met `find` voor krachtige bestandsverwerking.
- Wees voorzichtig met `rm` en andere destructieve commando's; gebruik `-p` om bevestiging te vragen voordat je de opdrachten uitvoert.