# [Linux] C Shell (csh) fc gebruik: Geschiedenis van commando's bewerken

## Overzicht
De `fc`-opdracht in C Shell (csh) wordt gebruikt om eerder ingevoerde commando's te bewerken en opnieuw uit te voeren. Het biedt een handige manier om fouten te corrigeren of om variaties van eerdere commando's te proberen zonder ze opnieuw volledig in te voeren.

## Gebruik
De basis syntaxis van de `fc`-opdracht is als volgt:

```csh
fc [opties] [argumenten]
```

## Veelvoorkomende opties
- `-l`: Lijst de geschiedenis van commando's.
- `-e`: Specificeer een editor om de commando's te bewerken.
- `-n`: Voorkom dat de regels met commando's worden genummerd bij het weergeven.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Laat de laatste 5 commando's zien
```csh
fc -l -5
```

### Voorbeeld 2: Bewerk het laatste commando met de standaard editor
```csh
fc
```

### Voorbeeld 3: Bewerk een specifiek commando met een opgegeven editor
```csh
fc -e vi 10
```
Hierbij wordt het 10e commando in de geschiedenis geopend in de `vi` editor.

### Voorbeeld 4: Voer het laatste commando opnieuw uit
```csh
fc -s
```

## Tips
- Gebruik `fc -l` om snel een overzicht van je commando geschiedenis te krijgen.
- Als je vaak dezelfde commando's bewerkt, overweeg dan om een specifieke editor in te stellen voor `fc` om je workflow te versnellen.
- Vergeet niet dat je met `fc` ook commando's kunt combineren en aanpassen voordat je ze opnieuw uitvoert, wat tijd kan besparen.