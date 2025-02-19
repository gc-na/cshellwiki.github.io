# [Linux] C Shell (csh) getopts gebruik: [verwerken van commandoregelopties]

## Overzicht
De `getopts`-opdracht in C Shell (csh) wordt gebruikt om commandoregelopties te parseren. Het stelt scripts in staat om opties en argumenten van de gebruiker te verwerken, waardoor ze flexibeler en gebruiksvriendelijker worden.

## Gebruik
De basis syntaxis van de `getopts`-opdracht is als volgt:

```csh
getopts optstring variable
```

Hierbij is `optstring` een string die de beschikbare opties definieert, en `variable` is de naam van de variabele waarin de huidige optie wordt opgeslagen.

## Veelvoorkomende opties
- `optstring`: Een string die de opties definieert. Elke optie wordt weergegeven door een enkele letter. Opties die een argument vereisen, worden gevolgd door een dubbele punt (bijvoorbeeld `a:`).
- `variable`: De naam van de variabele waarin de huidige optie wordt opgeslagen.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Eenvoudige opties
Dit voorbeeld toont hoe je eenvoudige opties kunt verwerken.

```csh
#!/bin/csh
set optstring = "ab"
while (getopts $optstring opt)
    switch ($opt)
        case "a":
            echo "Optie A geselecteerd"
            breaksw
        case "b":
            echo "Optie B geselecteerd"
            breaksw
        default:
            echo "Ongeldige optie"
    endsw
end
```

### Voorbeeld 2: Opties met argumenten
Hier is een voorbeeld dat laat zien hoe je opties met argumenten kunt verwerken.

```csh
#!/bin/csh
set optstring = "a:b:"
while (getopts $optstring opt)
    switch ($opt)
        case "a":
            echo "Optie A met argument: $OPTARG"
            breaksw
        case "b":
            echo "Optie B met argument: $OPTARG"
            breaksw
        default:
            echo "Ongeldige optie"
    endsw
end
```

### Voorbeeld 3: Meerdere opties
Dit voorbeeld laat zien hoe je meerdere opties tegelijk kunt verwerken.

```csh
#!/bin/csh
set optstring = "abc"
while (getopts $optstring opt)
    echo "Geselecteerde optie: $opt"
end
```

## Tips
- Zorg ervoor dat je de opties goed definieert in de `optstring`, zodat gebruikers weten welke opties beschikbaar zijn.
- Gebruik de `switch`-structuur om de verschillende opties te verwerken, wat de leesbaarheid van je script verbetert.
- Vergeet niet om de variabele `$OPTARG` te gebruiken om toegang te krijgen tot argumenten die bij opties zijn opgegeven.