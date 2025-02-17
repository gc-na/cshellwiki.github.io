# [Linux] Bash shift gebruik: Verplaats argumenten naar links

## Overzicht
De `shift`-opdracht in Bash wordt gebruikt om de positie van de argumenten in de `$@`-array naar links te verschuiven. Dit betekent dat het eerste argument wordt verwijderd en de overige argumenten één positie naar voren worden geschoven. Dit is nuttig in scripts waar je door argumenten wilt itereren.

## Gebruik
De basis syntaxis van de `shift`-opdracht is als volgt:

```bash
shift [n]
```

Hierbij is `n` het aantal posities dat je wilt verschuiven. Als `n` niet wordt opgegeven, wordt standaard één positie verschoven.

## Veelvoorkomende opties
- `n`: Het aantal posities dat je wilt verschuiven. Als je bijvoorbeeld `shift 2` gebruikt, worden de eerste twee argumenten verwijderd.

## Veelvoorkomende voorbeelden

### Voorbeeld 1: Basisgebruik
```bash
#!/bin/bash
echo "Originele argumenten: $@"
shift
echo "Na shift: $@"
```
In dit voorbeeld worden de originele argumenten weergegeven en daarna wordt het eerste argument verwijderd.

### Voorbeeld 2: Meerdere posities verschuiven
```bash
#!/bin/bash
echo "Originele argumenten: $@"
shift 2
echo "Na shift 2: $@"
```
Hier worden de eerste twee argumenten verwijderd en de resterende argumenten worden weergegeven.

### Voorbeeld 3: Argumenten verwerken in een loop
```bash
#!/bin/bash
while [[ $# -gt 0 ]]; do
    echo "Huidig argument: $1"
    shift
done
```
In dit voorbeeld worden alle argumenten één voor één weergegeven totdat er geen argumenten meer zijn.

## Tips
- Gebruik `shift` in combinatie met loops om eenvoudig door argumenten te itereren.
- Wees voorzichtig met het aantal posities dat je verschuift; als je meer verschuift dan er argumenten zijn, kunnen er lege waarden ontstaan.
- Het is handig om een controle in te bouwen om te controleren of er nog argumenten zijn voordat je `shift` gebruikt, bijvoorbeeld door `[[ $# -gt 0 ]]` te controleren.