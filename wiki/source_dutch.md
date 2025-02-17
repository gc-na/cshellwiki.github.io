# [Linux] Bash source gebruik: Voer een script uit in de huidige shell

## Overzicht
De `source`-opdracht in Bash wordt gebruikt om een script of een bestand met shell-commando's uit te voeren in de huidige shellomgeving. Dit betekent dat alle variabelen en functies die in het script zijn gedefinieerd, beschikbaar blijven na de uitvoering.

## Gebruik
De basis syntaxis van de `source`-opdracht is als volgt:

```bash
source [opties] [argumenten]
```

## Veelvoorkomende opties
- **-h, --help**: Toon een helpbericht met informatie over het gebruik van de opdracht.
- **-V, --version**: Toon de versie-informatie van de shell.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Een script uitvoeren
Om een script genaamd `myscript.sh` uit te voeren, gebruik je:

```bash
source myscript.sh
```

### Voorbeeld 2: Een configuratiebestand laden
Je kunt een configuratiebestand, zoals `.bashrc`, laden om de instellingen in de huidige shell toe te passen:

```bash
source ~/.bashrc
```

### Voorbeeld 3: Een functie definiëren en gebruiken
Stel dat je een script hebt dat een functie definieert. Je kunt het script uitvoeren met `source` en vervolgens de functie aanroepen:

```bash
# myfunctions.sh
function greet {
    echo "Hallo, $1!"
}

# Voer het script uit
source myfunctions.sh

# Roep de functie aan
greet "wereld"
```

## Tips
- Gebruik `source` in plaats van `./` om ervoor te zorgen dat variabelen en functies beschikbaar blijven in de huidige shell.
- Controleer altijd de uitvoer van je scripts om ervoor te zorgen dat er geen fouten zijn opgetreden.
- Maak gebruik van commentaar in je scripts om de functionaliteit en het doel van verschillende secties duidelijk te maken.