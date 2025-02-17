# [Linux] Bash if gebruik: Voorwaardelijke uitvoering van commando's

## Overzicht
De `if`-opdracht in Bash wordt gebruikt om voorwaardelijke logica in scripts te implementeren. Hiermee kun je bepalen welke commando's moeten worden uitgevoerd op basis van de evaluatie van een bepaalde voorwaarde.

## Gebruik
De basis syntaxis van de `if`-opdracht is als volgt:

```bash
if [ voorwaarde ]; then
    # commando's die uitgevoerd worden als de voorwaarde waar is
fi
```

## Veelvoorkomende opties
- `-e`: Controleert of een bestand bestaat.
- `-d`: Controleert of een directory bestaat.
- `-f`: Controleert of een bestand een regulier bestand is.
- `-z`: Controleert of een string leeg is.
- `-n`: Controleert of een string niet leeg is.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Bestaan van een bestand controleren
```bash
if [ -e "bestand.txt" ]; then
    echo "Het bestand bestaat."
else
    echo "Het bestand bestaat niet."
fi
```

### Voorbeeld 2: Controleer of een directory bestaat
```bash
if [ -d "mijn_map" ]; then
    echo "De map bestaat."
else
    echo "De map bestaat niet."
fi
```

### Voorbeeld 3: Controleer of een variabele leeg is
```bash
VAR=""
if [ -z "$VAR" ]; then
    echo "De variabele is leeg."
else
    echo "De variabele is niet leeg."
fi
```

### Voorbeeld 4: Vergelijking van getallen
```bash
a=5
b=10
if [ $a -lt $b ]; then
    echo "$a is kleiner dan $b."
fi
```

## Tips
- Zorg ervoor dat je spaties gebruikt rondom de haakjes in de `if`-opdracht, anders kan de syntaxis fout zijn.
- Gebruik `elif` voor meerdere voorwaarden en `else` voor alternatieve acties.
- Test je scripts grondig om ervoor te zorgen dat de voorwaarden correct worden geëvalueerd.