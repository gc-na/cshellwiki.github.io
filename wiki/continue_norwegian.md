# [Linux] Bash continue bruken: Fortsetter løkken i skripting

## Oversikt
`continue`-kommandoen brukes i Bash-skript for å hoppe over den gjeldende iterasjonen av en løkke og fortsette med neste iterasjon. Dette er nyttig når du ønsker å unngå spesifikke betingelser uten å avslutte hele løkken.

## Bruk
Den grunnleggende syntaksen for `continue`-kommandoen er:

```bash
continue [n]
```

Her representerer `n` antall nivåer av løkker som skal hoppes over, der `1` er den innerste løkken.

## Vanlige alternativer
- `n`: Angir hvor mange nivåer av løkker som skal hoppes over. Hvis ikke spesifisert, hopper den over den innerste løkken.

## Vanlige eksempler

### Eksempel 1: Hopp over spesifikke verdier i en for-løkke
```bash
for i in {1..10}; do
    if [ $i -eq 5 ]; then
        continue
    fi
    echo "Tall: $i"
done
```
I dette eksemplet vil tallet 5 bli hoppet over, og utskriften vil vise tallene 1 til 10, unntatt 5.

### Eksempel 2: Hopp over negative tall i en while-løkke
```bash
tall=0
while [ $tall -le 10 ]; do
    tall=$((tall - 1))
    if [ $tall -lt 0 ]; then
        continue
    fi
    echo "Ikke-negative tall: $tall"
done
```
Her vil løkken hoppe over negative tall, og bare ikke-negative tall vil bli skrevet ut.

### Eksempel 3: Bruke continue i en nested løkke
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
I dette tilfellet vil `j`-verdien 2 bli hoppet over for hver `i`, og utskriften vil vise kombinasjoner av `i` og `j`, unntatt når `j` er 2.

## Tips
- Bruk `continue` for å forbedre lesbarheten av skriptene dine ved å unngå unødvendige nestede `if`-setninger.
- Vær oppmerksom på hvilken løkke `continue` påvirker, spesielt i skript med flere nivåer av løkker.
- Test skriptene dine grundig for å sikre at `continue` oppfører seg som forventet, spesielt når du arbeider med komplekse betingelser.