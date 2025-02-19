# [Linux] C Shell (csh) stty gebruik: Instellen van terminal eigenschappen

## Overzicht
De `stty`-opdracht wordt gebruikt om de eigenschappen van de terminal in te stellen en te wijzigen. Hiermee kun je verschillende instellingen configureren, zoals invoer- en uitvoerinstellingen, speciale toetsen en meer.

## Gebruik
De basis syntaxis van de `stty`-opdracht is als volgt:

```csh
stty [opties] [argumenten]
```

## Veelvoorkomende opties
- `-a`: Toont alle huidige instellingen van de terminal.
- `-g`: Geeft de huidige instellingen weer in een formaat dat later kan worden hersteld.
- `erase`: Stelt het teken in dat gebruikt wordt om een teken te wissen.
- `kill`: Stelt het teken in dat gebruikt wordt om de huidige regel te wissen.
- `intr`: Stelt het teken in dat gebruikt wordt om een onderbreking te genereren (bijv. Ctrl+C).

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `stty`:

### Huidige instellingen weergeven
Om de huidige instellingen van de terminal weer te geven, gebruik je:

```csh
stty -a
```

### Instellen van het wis-teken
Om het wis-teken in te stellen op de backspace-toets, gebruik je:

```csh
stty erase ^H
```

### Instellen van het onderbrekingsteken
Om het onderbrekingsteken in te stellen op Ctrl+C, gebruik je:

```csh
stty intr ^C
```

### Instellingen opslaan en herstellen
Om de huidige instellingen op te slaan en later te herstellen, gebruik je:

```csh
stty -g > instellingen.txt
# Later herstellen
stty $(<instellingen.txt)
```

## Tips
- Controleer altijd de huidige instellingen met `stty -a` voordat je wijzigingen aanbrengt.
- Wees voorzichtig met het instellen van speciale toetsen, omdat dit de werking van je terminal kan beïnvloeden.
- Gebruik de `-g` optie om instellingen op te slaan voor toekomstig gebruik, vooral als je vaak met verschillende terminals werkt.