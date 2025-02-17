# [Linux] Bash break brug: Afbryd en loop

## Oversigt
`break`-kommandoen bruges i Bash-scripts til at afslutte en loop tidligt. Når `break` udføres, stopper den den aktuelle loop, og kontrol overgår til den næste kommando efter loopet.

## Brug
Den grundlæggende syntaks for `break`-kommandoen er:

```bash
break [n]
```

Her angiver `n` antallet af niveauer af loops, der skal afsluttes. Hvis `n` ikke angives, afsluttes kun den inderste loop.

## Almindelige muligheder
- `n`: Angiver hvor mange niveauer af loops der skal afsluttes. Hvis der er flere indlejrede loops, kan du bruge denne mulighed til at afslutte flere niveauer.

## Almindelige eksempler

### Eksempel 1: Afbryd en enkel loop
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        break
    fi
    echo "Nummer: $i"
done
```
*Output:*
```
Nummer: 1
Nummer: 2
```

### Eksempel 2: Afbryd en indlejret loop
```bash
for i in {1..3}; do
    for j in {1..3}; do
        if [ $j -eq 2 ]; then
            break 2
        fi
        echo "i: $i, j: $j"
    done
done
```
*Output:*
```
i: 1, j: 1
```

### Eksempel 3: Brug af break i en while loop
```bash
count=1
while true; do
    echo "Tæller: $count"
    if [ $count -ge 5 ]; then
        break
    fi
    ((count++))
done
```
*Output:*
```
Tæller: 1
Tæller: 2
Tæller: 3
Tæller: 4
Tæller: 5
```

## Tips
- Brug `break` i indlejrede loops for at kontrollere, hvilken loop der skal afsluttes ved at angive et niveau.
- Vær opmærksom på, at `break` kun afslutter loops og ikke betingede udsagn som `if` eller `case`.
- Test altid dine scripts i et sikkert miljø for at sikre, at `break` fungerer som forventet, især i komplekse loop-strukturer.