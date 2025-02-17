# [Linux] Bash else gebruik: Voorwaardelijke uitvoering in scripts

## Overzicht
De `else`-opdracht in Bash wordt gebruikt binnen een `if`-structuur om alternatieve commando's uit te voeren wanneer de voorwaarde van de `if`-verklaring niet waar is. Het stelt gebruikers in staat om verschillende paden in hun scripts te volgen op basis van voorwaarden.

## Gebruik
De basisstructuur van de `else`-opdracht is als volgt:

```bash
if [ voorwaarde ]; then
    # commando's als de voorwaarde waar is
else
    # commando's als de voorwaarde niet waar is
fi
```

## Veelvoorkomende Opties
De `else`-opdracht zelf heeft geen specifieke opties, maar het wordt vaak gebruikt in combinatie met de `if`-opdracht. Hier zijn enkele veelvoorkomende voorwaarden die je kunt gebruiken:

- `[ -f bestand ]`: Controleert of een bestand bestaat.
- `[ -d map ]`: Controleert of een map bestaat.
- `[ -z string ]`: Controleert of een string leeg is.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Bestandscontrole
```bash
if [ -f mijnbestand.txt ]; then
    echo "Bestand bestaat."
else
    echo "Bestand bestaat niet."
fi
```

### Voorbeeld 2: Mapcontrole
```bash
if [ -d mijnmap ]; then
    echo "Map bestaat."
else
    echo "Map bestaat niet."
fi
```

### Voorbeeld 3: Stringcontrole
```bash
input=""

if [ -z "$input" ]; then
    echo "De string is leeg."
else
    echo "De string is niet leeg."
fi
```

## Tips
- Zorg ervoor dat je de juiste spaties gebruikt in je voorwaarden; de syntaxis is gevoelig voor spaties.
- Gebruik haakjes om complexe voorwaarden te groeperen, bijvoorbeeld: `if [ -f bestand ] && [ -r bestand ]; then`.
- Test je scripts met verschillende scenario's om ervoor te zorgen dat de `else`-structuur correct werkt.