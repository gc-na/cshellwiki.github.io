# [Linux] C Shell (csh) export gebruik: Omgevingsvariabelen instellen

## Overzicht
De `export` opdracht in C Shell (csh) wordt gebruikt om omgevingsvariabelen in te stellen en beschikbaar te maken voor subprocessen. Dit betekent dat wanneer je een variabele exporteert, deze toegankelijk is voor alle programma's die vanuit de huidige shell worden uitgevoerd.

## Gebruik
De basis syntaxis van de `export` opdracht is als volgt:

```csh
export [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n`: Verwijdert de exportstatus van een variabele.
- `-p`: Toont een lijst van alle geëxporteerde variabelen.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Een variabele exporteren
```csh
set VARIABEL = "waarde"
export VARIABEL
```
In dit voorbeeld wordt de variabele `VARIABEL` ingesteld op "waarde" en vervolgens geëxporteerd, zodat deze beschikbaar is voor subprocessen.

### Voorbeeld 2: Meerdere variabelen exporteren
```csh
set VAR1 = "waarde1"
set VAR2 = "waarde2"
export VAR1 VAR2
```
Hier worden zowel `VAR1` als `VAR2` geëxporteerd, zodat beide variabelen toegankelijk zijn voor andere programma's.

### Voorbeeld 3: Exporteren met de -n optie
```csh
export -n VARIABEL
```
Met deze opdracht wordt de exportstatus van `VARIABEL` verwijderd, waardoor deze niet langer beschikbaar is voor subprocessen.

### Voorbeeld 4: Lijst van geëxporteerde variabelen
```csh
export -p
```
Dit toont een lijst van alle momenteel geëxporteerde variabelen in de shell.

## Tips
- Zorg ervoor dat je variabelen een duidelijke naam hebben om verwarring te voorkomen.
- Gebruik de `-p` optie regelmatig om te controleren welke variabelen zijn geëxporteerd.
- Vergeet niet dat geëxporteerde variabelen alleen beschikbaar zijn voor subprocessen, niet voor de huidige shell.