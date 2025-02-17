# [Linux] Bash endif gebruik: Beëindig een voorwaardelijke instructie

## Overzicht
De `endif`-opdracht in Bash wordt gebruikt om het einde van een voorwaardelijke instructie aan te geven, zoals een `if`-verklaring. Het is geen zelfstandige opdracht, maar een syntactisch element dat de structuur van een script definieert.

## Gebruik
De basisstructuur van een `if`-verklaring met `endif` ziet er als volgt uit:

```bash
if [ voorwaarde ]; then
    # opdrachten
fi
```

In plaats van `fi` kan in sommige programmeertalen `endif` worden gebruikt, maar in Bash is `fi` de correcte afsluiting.

## Veelvoorkomende opties
- `then`: Dit geeft het begin aan van de opdrachten die uitgevoerd moeten worden als de voorwaarde waar is.
- `else`: Dit geeft de alternatieve opdrachten aan die uitgevoerd moeten worden als de voorwaarde niet waar is.
- `elif`: Dit staat toe om extra voorwaarden toe te voegen.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Eenvoudige if-verklaring
```bash
if [ $a -gt 10 ]; then
    echo "a is groter dan 10"
fi
```

### Voorbeeld 2: if-else-verklaring
```bash
if [ $a -gt 10 ]; then
    echo "a is groter dan 10"
else
    echo "a is 10 of kleiner"
fi
```

### Voorbeeld 3: if-elif-else-verklaring
```bash
if [ $a -gt 10 ]; then
    echo "a is groter dan 10"
elif [ $a -eq 10 ]; then
    echo "a is gelijk aan 10"
else
    echo "a is kleiner dan 10"
fi
```

## Tips
- Zorg ervoor dat je de juiste syntaxis gebruikt; in Bash gebruik je `fi` om een `if`-verklaring af te sluiten.
- Gebruik spaties rond de haakjes in de voorwaarde om syntaxisfouten te voorkomen.
- Test je scripts met verschillende waarden om ervoor te zorgen dat alle voorwaarden correct worden afgehandeld.