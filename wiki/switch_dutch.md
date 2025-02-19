# [Linux] C Shell (csh) switch gebruik: Schakel tussen verschillende opties

## Overzicht
De `switch`-opdracht in C Shell (csh) wordt gebruikt om verschillende opties of gevallen te evalueren. Het is een manier om conditionele logica in scripts te implementeren, waardoor je verschillende acties kunt uitvoeren op basis van de waarde van een variabele.

## Gebruik
De basis syntaxis van de `switch`-opdracht is als volgt:

```csh
switch (uitdrukking)
    case patroon1:
        commando's
        breaksw
    case patroon2:
        commando's
        breaksw
    default:
        commando's
        breaksw
endsw
```

## Veelvoorkomende Opties
- `case`: Definieert een patroon dat vergeleken wordt met de uitdrukking.
- `breaksw`: Beëindigt de huidige `switch`-structuur.
- `default`: Voert commando's uit als geen van de patronen overeenkomt met de uitdrukking.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Eenvoudige switch
```csh
set kleur = "rood"
switch ($kleur)
    case "rood":
        echo "De kleur is rood."
        breaksw
    case "blauw":
        echo "De kleur is blauw."
        breaksw
    default:
        echo "Onbekende kleur."
        breaksw
endsw
```

### Voorbeeld 2: Meerdere patronen
```csh
set fruit = "appel"
switch ($fruit)
    case "appel":
    case "peer":
        echo "Dit is een vrucht."
        breaksw
    default:
        echo "Dit is geen vrucht."
        breaksw
endsw
```

### Voorbeeld 3: Gebruik van variabelen
```csh
set getal = 2
switch ($getal)
    case 1:
        echo "Het getal is één."
        breaksw
    case 2:
        echo "Het getal is twee."
        breaksw
    case 3:
        echo "Het getal is drie."
        breaksw
    default:
        echo "Onbekend getal."
        breaksw
endsw
```

## Tips
- Zorg ervoor dat je altijd een `default`-optie toevoegt om onverwachte waarden af te handelen.
- Gebruik `breaksw` om ervoor te zorgen dat je niet per ongeluk doorloopt naar andere cases.
- Test je `switch`-structuren met verschillende invoerwaarden om ervoor te zorgen dat ze correct functioneren.