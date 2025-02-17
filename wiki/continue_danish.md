# [Linux] Bash continue brug: Fortsæt med næste iteration i en løkke

## Oversigt
`continue`-kommandoen bruges i Bash-scripts til at springe den resterende del af den aktuelle iteration i en løkke over og fortsætte med den næste iteration. Dette er nyttigt, når du vil undgå at udføre visse kommandoer under specifikke betingelser.

## Brug
Den grundlæggende syntaks for `continue`-kommandoen er:

```bash
continue [n]
```

Her angiver `n`, hvor mange iterationer der skal springes over. Hvis `n` ikke er angivet, springes kun den aktuelle iteration over.

## Almindelige muligheder
- `n`: Angiver hvor mange iterationer der skal springes over. Standard er 1, hvilket betyder, at kun den aktuelle iteration springes over.

## Almindelige eksempler

### Eksempel 1: Spring over lige tal i en løkke
```bash
for i in {1..10}; do
    if (( i % 2 == 0 )); then
        continue
    fi
    echo $i
done
```
Dette script vil kun udskrive de ulige tal fra 1 til 10.

### Eksempel 2: Spring over bestemte værdier
```bash
for i in {1..10}; do
    if [ $i -eq 5 ]; then
        continue
    fi
    echo $i
done
```
Her vil tallet 5 blive sprunget over, og alle andre tal fra 1 til 10 vil blive udskrevet.

### Eksempel 3: Brug af continue i en while-løkke
```bash
count=0
while [ $count -lt 10 ]; do
    count=$((count + 1))
    if [ $count -eq 7 ]; then
        continue
    fi
    echo $count
done
```
Dette script vil udskrive tallene fra 1 til 10, men vil springe over tallet 7.

## Tips
- Brug `continue` til at forbedre læsbarheden af dit script ved at undgå indlejrede betingelser.
- Vær opmærksom på, at `continue` kun påvirker den nærmeste løkke, så hvis du har indlejrede løkker, vil det kun springe iterationen i den inderste løkke over.
- Test altid dit script med forskellige inddata for at sikre, at `continue` fungerer som forventet.