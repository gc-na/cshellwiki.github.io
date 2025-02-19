# [Linux] C Shell (csh) else: Voer alternatieve commando's uit

## Overzicht
De `else`-opdracht in C Shell (csh) wordt gebruikt in combinatie met de `if`-structuur om alternatieve commando's uit te voeren wanneer de voorwaarde van de `if`-verklaring niet waar is. Dit maakt het mogelijk om verschillende acties te ondernemen op basis van de uitkomst van een voorwaarde.

## Gebruik
De basis syntaxis van de `else`-opdracht is als volgt:

```
if (voorwaarde) then
    commando1
else
    commando2
endif
```

## Veelvoorkomende opties
De `else`-opdracht zelf heeft geen specifieke opties, omdat het voornamelijk een onderdeel is van de controleflow in scripts. Het is echter belangrijk om de `if`-structuur correct te gebruiken.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Eenvoudige if-else
```csh
set VAR = 10
if ($VAR > 5) then
    echo "VAR is groter dan 5"
else
    echo "VAR is 5 of kleiner"
endif
```

### Voorbeeld 2: Controle op een bestand
```csh
if (-e bestand.txt) then
    echo "Het bestand bestaat."
else
    echo "Het bestand bestaat niet."
endif
```

### Voorbeeld 3: Alternatieve uitvoer
```csh
set NUM = 3
if ($NUM == 1) then
    echo "Num is één."
else
    echo "Num is niet één."
endif
```

## Tips
- Zorg ervoor dat je de `endif`-verklaring niet vergeet om de `if`-structuur correct af te sluiten.
- Gebruik haakjes om de voorwaarden duidelijk te maken en om fouten te voorkomen.
- Test je scripts met verschillende invoerwaarden om te controleren of de `else`-structuur correct werkt.