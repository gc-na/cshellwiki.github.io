# [Linux] Bash continue gebruik: Voortzetten van een loop

## Overzicht
De `continue` opdracht in Bash wordt gebruikt om de huidige iteratie van een loop over te slaan en door te gaan naar de volgende iteratie. Dit is handig wanneer je bepaalde voorwaarden wilt negeren zonder de hele loop te beëindigen.

## Gebruik
De basis syntaxis van de `continue` opdracht is als volgt:

```bash
continue [n]
```

Hierbij is `n` een optioneel argument dat aangeeft hoeveel iteraties van de loop moeten worden overgeslagen. Als `n` niet wordt opgegeven, wordt de huidige iteratie overgeslagen en gaat de loop verder met de volgende iteratie.

## Veelvoorkomende opties
- `n`: Een optioneel argument dat het aantal iteraties aangeeft dat moet worden overgeslagen. Standaard is dit 1.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Basisgebruik van continue
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        continue
    fi
    echo $i
done
```
In dit voorbeeld worden de getallen 1, 2, 4 en 5 afgedrukt. Het getal 3 wordt overgeslagen.

### Voorbeeld 2: Continue in een while-lus
```bash
count=0
while [ $count -lt 5 ]; do
    count=$((count + 1))
    if [ $count -eq 2 ]; then
        continue
    fi
    echo $count
done
```
Hier wordt ook het getal 2 overgeslagen, en de uitvoer zal 1, 3, 4 en 5 zijn.

### Voorbeeld 3: Gebruik van continue met een geneste loop
```bash
for i in {1..3}; do
    for j in {1..3}; do
        if [ $j -eq 2 ]; then
            continue
        fi
        echo "i: $i, j: $j"
    done
done
```
In dit geval worden de combinaties van `i` en `j` afgedrukt, maar de waarde `j=2` wordt overgeslagen.

## Tips
- Gebruik `continue` om de leesbaarheid van je code te verbeteren door onnodige geneste if-statements te vermijden.
- Wees voorzichtig met het gebruik van `continue` in geneste loops; zorg ervoor dat je weet welke loop je beïnvloedt.
- Test je loops grondig om ervoor te zorgen dat de juiste iteraties worden overgeslagen en dat je geen onverwachte resultaten krijgt.