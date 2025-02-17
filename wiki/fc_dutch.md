# [Linux] Bash fc gebruik: Geschiedenis van commando's bewerken

## Overzicht
De `fc` (fix command) opdracht in Bash wordt gebruikt om eerder ingevoerde commando's te bekijken en te bewerken. Het stelt gebruikers in staat om hun commandoregelgeschiedenis te doorlopen en specifieke commando's te corrigeren of opnieuw uit te voeren.

## Gebruik
De basis syntaxis van de `fc` opdracht is als volgt:

```bash
fc [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-l`: Lijst de geschiedenis van commando's.
- `-r`: Lijst de geschiedenis in omgekeerde volgorde.
- `-s`: Voer het laatste commando uit zonder het te bewerken.
- `-n`: Toon geen nummering bij het weergeven van de geschiedenis.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `fc` opdracht:

### Voorbeeld 1: Lijst de laatste 10 commando's
```bash
fc -l -n -10
```

### Voorbeeld 2: Bewerk het laatste commando
```bash
fc
```
Dit opent het laatste commando in de standaard teksteditor.

### Voorbeeld 3: Voer het laatste commando uit zonder bewerken
```bash
fc -s
```

### Voorbeeld 4: Lijst de geschiedenis in omgekeerde volgorde
```bash
fc -r -l 10
```

## Tips
- Gebruik `fc` regelmatig om snel fouten in eerder ingevoerde commando's te corrigeren.
- Combineer `fc` met andere shell-functies zoals pijpen om de efficiëntie te verhogen.
- Vergeet niet dat de geschiedenis van commando's kan worden doorzocht met `history`, wat een nuttige aanvulling kan zijn op `fc`.