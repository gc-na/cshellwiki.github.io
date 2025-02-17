# [Linux] Bash test gebruik: Voer evaluaties uit op bestanden en variabelen

## Overzicht
De `test` opdracht in Bash wordt gebruikt om evaluaties uit te voeren op bestanden en variabelen. Het helpt bij het controleren van voorwaarden, zoals of een bestand bestaat, of een variabele leeg is, of twee waarden gelijk zijn, en meer. Dit is vooral nuttig in scripts om beslissingen te nemen op basis van de resultaten van deze evaluaties.

## Gebruik
De basis syntaxis van de `test` opdracht is als volgt:

```bash
test [opties] [argumenten]
```

## Veelvoorkomende opties
Hier zijn enkele veelgebruikte opties voor de `test` opdracht:

- `-e bestand`: Controleert of het opgegeven bestand bestaat.
- `-f bestand`: Controleert of het opgegeven bestand een regulier bestand is.
- `-d map`: Controleert of het opgegeven pad een directory is.
- `-z string`: Controleert of de opgegeven string leeg is.
- `string1 = string2`: Controleert of twee strings gelijk zijn.
- `n1 -eq n2`: Controleert of twee getallen gelijk zijn.

## Veelvoorkomende voorbeelden

Hier zijn enkele praktische voorbeelden van het gebruik van de `test` opdracht:

### Voorbeeld 1: Controleer of een bestand bestaat
```bash
if test -e mijn_bestand.txt; then
    echo "Het bestand bestaat."
else
    echo "Het bestand bestaat niet."
fi
```

### Voorbeeld 2: Controleer of een variabele leeg is
```bash
variabele=""
if test -z "$variabele"; then
    echo "De variabele is leeg."
else
    echo "De variabele is niet leeg."
fi
```

### Voorbeeld 3: Vergelijk twee getallen
```bash
getal1=10
getal2=20
if test $getal1 -lt $getal2; then
    echo "$getal1 is kleiner dan $getal2."
fi
```

### Voorbeeld 4: Controleer of een pad een directory is
```bash
if test -d /pad/naar/map; then
    echo "Dit is een directory."
else
    echo "Dit is geen directory."
fi
```

## Tips
- Gebruik de `[` en `]` haakjes als een alternatieve syntaxis voor `test`, bijvoorbeeld: `[ -e mijn_bestand.txt ]`.
- Zorg ervoor dat je spaties gebruikt rondom de haakjes en operators voor een correcte syntaxis.
- Combineer meerdere voorwaarden met `-a` (en) of `-o` (of) voor complexere evaluaties.