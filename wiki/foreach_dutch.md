# [Linux] C Shell (csh) foreach gebruik: Itereren over een lijst van items

## Overzicht
De `foreach`-opdracht in C Shell (csh) wordt gebruikt om een reeks commando's uit te voeren voor elk item in een lijst. Dit maakt het mogelijk om repetitieve taken te automatiseren en efficiënt te werken met meerdere bestanden of variabelen.

## Gebruik
De basis syntaxis van de `foreach`-opdracht is als volgt:

```csh
foreach variabele (lijst)
    commando's
end
```

## Veelvoorkomende Opties
- **variabele**: De naam van de variabele die elk item in de lijst zal bevatten.
- **lijst**: Een lijst van items of bestanden die doorlopen moeten worden.
- **commando's**: De commando's die uitgevoerd moeten worden voor elk item in de lijst.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Basisgebruik
Dit voorbeeld toont hoe je een lijst van bestanden kunt doorlopen en hun namen kunt afdrukken.

```csh
foreach bestand (*)
    echo $bestand
end
```

### Voorbeeld 2: Bewerken van bestanden
Hierdoor kun je een reeks tekstbestanden doorlopen en een bepaalde bewerking uitvoeren, zoals het kopiëren naar een andere map.

```csh
foreach bestand (*.txt)
    cp $bestand /pad/naar/doelmap/
end
```

### Voorbeeld 3: Itereren met een variabele
In dit voorbeeld worden de getallen van 1 tot 5 doorlopen en wordt elk getal verdubbeld.

```csh
foreach nummer (1 2 3 4 5)
    @ dubbel = $nummer * 2
    echo $dubbel
end
```

## Tips
- Zorg ervoor dat je de `end`-instructie niet vergeet; dit is essentieel om de `foreach`-lus correct af te sluiten.
- Gebruik duidelijke en beschrijvende namen voor je variabelen om de leesbaarheid van je scripts te verbeteren.
- Test je `foreach`-commando's met een kleine lijst voordat je ze op een grotere dataset toepast om onbedoelde fouten te voorkomen.