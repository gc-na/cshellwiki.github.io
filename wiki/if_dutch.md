# [Unix] C Shell (csh) if gebruik: Voorwaardelijke uitvoering van commando's

## Overzicht
De `if`-opdracht in C Shell (csh) wordt gebruikt om voorwaardelijke logica toe te passen in scripts. Hiermee kun je bepaalde commando's uitvoeren op basis van de evaluatie van een voorwaarde.

## Gebruik
De basis syntaxis van de `if`-opdracht is als volgt:

```
if (voorwaarde) 
    commando
endif
```

## Veelvoorkomende Opties
- `-e`: Controleert of een bestand bestaat.
- `-d`: Controleert of een pad een directory is.
- `-f`: Controleert of een pad een regulier bestand is.
- `==`: Vergelijkt twee strings op gelijkheid.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Bestandscontrole
Controleer of een bestand bestaat en voer een commando uit.
```csh
if (-e bestand.txt) then
    echo "Het bestand bestaat."
endif
```

### Voorbeeld 2: Directorycontrole
Controleer of een pad een directory is.
```csh
if (-d /pad/naar/directory) then
    echo "Dit is een directory."
endif
```

### Voorbeeld 3: Stringvergelijking
Vergelijk twee strings.
```csh
set naam = "John"
if ("$naam" == "John") then
    echo "Hallo John!"
endif
```

### Voorbeeld 4: Meerdere voorwaarden
Gebruik geneste `if`-structuren voor complexere logica.
```csh
if (-e bestand.txt) then
    echo "Het bestand bestaat."
else if (-e ander_bestand.txt) then
    echo "Het andere bestand bestaat."
else
    echo "Geen van beide bestanden bestaat."
endif
```

## Tips
- Zorg ervoor dat je de juiste haakjes gebruikt bij de voorwaarden.
- Gebruik duidelijke en beschrijvende namen voor je variabelen om de leesbaarheid te verbeteren.
- Test je scripts met verschillende voorwaarden om onvoorziene fouten te voorkomen.