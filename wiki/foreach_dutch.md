# [Linux] Bash foreach gebruik: Itereren over een lijst van elementen

## Overzicht
De `foreach`-opdracht in Bash is een constructie die wordt gebruikt om over een lijst van elementen te itereren. Het is handig voor het uitvoeren van een bepaalde actie op elk element in de lijst.

## Gebruik
De basis syntaxis van de `foreach`-opdracht is als volgt:

```bash
foreach element in lijst; do
    # commando's om uit te voeren
done
```

## Veelvoorkomende opties
- `-n`: Voorkomt dat de uitvoer naar het scherm wordt gestuurd.
- `-e`: Voert een enkele regel uit als een commando.
- `-v`: Geeft de variabelen weer die worden gebruikt in de loop.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Eenvoudige iteratie
Dit voorbeeld toont hoe je door een lijst van getallen kunt itereren en ze kunt afdrukken.

```bash
foreach i in 1 2 3 4 5; do
    echo "Nummer: $i"
done
```

### Voorbeeld 2: Bestanden verwerken
Hier is een voorbeeld dat door een lijst van bestanden iterert en hun inhoud weergeeft.

```bash
foreach file in *.txt; do
    echo "Inhoud van $file:"
    cat $file
done
```

### Voorbeeld 3: Combineren met andere commando's
In dit voorbeeld worden bestanden gekopieerd naar een andere map.

```bash
foreach file in *.jpg; do
    cp $file /pad/naar/doelmap/
done
```

## Tips
- Zorg ervoor dat je de juiste syntaxis gebruikt, anders kan de loop niet correct functioneren.
- Gebruik haakjes om de lijst van elementen duidelijk te scheiden.
- Test je commando's met een kleine dataset voordat je ze op een grotere schaal toepast om onbedoelde fouten te voorkomen.