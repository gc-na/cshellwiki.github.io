# [Linux] Bash break gebruik: Stop een loop

## Overzicht
De `break` opdracht in Bash wordt gebruikt om een loop te beëindigen. Wanneer `break` wordt aangeroepen, stopt de uitvoering van de loop waarin het zich bevindt, en gaat het script verder met de volgende instructie na de loop.

## Gebruik
De basis syntaxis van de `break` opdracht is als volgt:

```bash
break [n]
```

Hierbij is `n` een optioneel argument dat aangeeft hoeveel niveaus van geneste loops moeten worden beëindigd. Als `n` niet wordt opgegeven, wordt alleen de meest binnenste loop beëindigd.

## Veelvoorkomende opties
- `n`: Het aantal niveaus van loops dat moet worden beëindigd. Standaard is dit 1.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Eenvoudige loop beëindigen
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo $i
done
```
In dit voorbeeld wordt de loop beëindigd wanneer `i` gelijk is aan 3. De uitvoer zal zijn:
```
1
2
```

### Voorbeeld 2: Geneste loops beëindigen
```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      break 2
    fi
    echo "$i, $j"
  done
done
```
Hier wordt de binnenste loop beëindigd wanneer `j` gelijk is aan 2, en de buitenste loop ook, omdat `break 2` is gebruikt. De uitvoer zal zijn:
```
1, 1
```

### Voorbeeld 3: Loop met een while-structuur
```bash
count=1
while [ $count -le 5 ]; do
  if [ $count -eq 4 ]; then
    break
  fi
  echo $count
  ((count++))
done
```
In dit geval stopt de loop wanneer `count` gelijk is aan 4. De uitvoer zal zijn:
```
1
2
3
```

## Tips
- Gebruik `break` om loops efficiënt te beëindigen wanneer een bepaalde voorwaarde is bereikt, wat de leesbaarheid van je script verbetert.
- Wees voorzichtig met geneste loops en het gebruik van het `n` argument, omdat dit kan leiden tot onverwachte resultaten als je niet goed oplet.
- Test je scripts met verschillende waarden om te begrijpen hoe `break` zich gedraagt in verschillende situaties.