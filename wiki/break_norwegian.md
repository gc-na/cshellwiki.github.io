# [Linux] Bash break bruk: Avslutt en loop

## Oversikt
`break`-kommandoen i Bash brukes til å avslutte en loop tidlig. Når `break`-kommandoen blir kalt, stopper den den nåværende loopen og fortsetter med koden som følger etter loopen. Dette er nyttig når du ønsker å bryte ut av en loop basert på en bestemt betingelse.

## Bruk
Den grunnleggende syntaksen for `break`-kommandoen er:

```bash
break [n]
```

Her er `n` et valgfritt argument som spesifiserer hvor mange nivåer av looper som skal brytes. Hvis `n` ikke er spesifisert, bryter den ut av den innerste loopen.

## Vanlige alternativer
- `n`: Angir hvor mange nivåer av looper som skal brytes. Standardverdi er 1.

## Vanlige eksempler

### Eksempel 1: Bryte ut av en enkel for-løkke
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo "Tall: $i"
done
```
I dette eksempelet vil utskriften være:
```
Tall: 1
Tall: 2
```
Loopen avsluttes når `i` er lik 3.

### Eksempel 2: Bryte ut av en while-løkke
```bash
count=1
while true; do
  echo "Teller: $count"
  if [ $count -ge 4 ]; then
    break
  fi
  ((count++))
done
```
Her vil utskriften være:
```
Teller: 1
Teller: 2
Teller: 3
```
Loopen avsluttes når `count` er lik 4.

### Eksempel 3: Bryte ut av en nestet løkke
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
I dette tilfellet vil ingen utskrift bli vist, fordi `break 2` avslutter begge loopene.

## Tips
- Bruk `break` når du har en spesifikk betingelse for å stoppe loopen, for eksempel når du finner et bestemt element.
- Vær oppmerksom på at `break` kun påvirker den loopen der den blir kalt. Hvis du har nestede løkker, kan du bruke `break n` for å spesifisere hvor mange nivåer du ønsker å bryte ut av.
- For debugging kan det være nyttig å inkludere echo-kommandoer før `break` for å se hvilke betingelser som utløser avslutningen av loopen.