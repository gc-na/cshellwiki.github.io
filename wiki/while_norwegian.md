# [Linux] Bash while bruk: Gjør repetisjon av kommandoer

## Oversikt
`while`-kommandoen i Bash brukes til å utføre en blokk med kommandoer gjentatte ganger så lenge en spesifisert betingelse er sann. Dette er nyttig for oppgaver som krever repetisjon, for eksempel å vente på en tilstand eller iterere over en liste.

## Bruk
Den grunnleggende syntaksen for `while`-kommandoen er som følger:

```bash
while [ betingelse ]; do
    # kommandoer
done
```

## Vanlige alternativer
`while`-kommandoen har ikke mange alternativer, men det er viktig å forstå hvordan betingelsene fungerer. Her er noen vanlige måter å bruke betingelser på:

- `true`: Kjør kommandoene uendelig.
- `false`: Kjør aldri kommandoene.
- `test [betingelse]`: Bruk test for å evaluere en betingelse.

## Vanlige eksempler

### Eksempel 1: Enkel teller
Dette eksemplet viser hvordan man kan bruke `while` for å telle fra 1 til 5.

```bash
count=1
while [ $count -le 5 ]; do
    echo "Teller: $count"
    ((count++))
done
```

### Eksempel 2: Vente på en fil
Her er et eksempel på å vente på at en fil skal eksistere før man fortsetter.

```bash
while [ ! -f "fil.txt" ]; do
    echo "Venter på fil.txt..."
    sleep 2
done
echo "Fil funnet!"
```

### Eksempel 3: Iterere over en liste
I dette eksemplet itererer vi over en liste med elementer.

```bash
liste=("eple" "banan" "kirsebær")
index=0
while [ $index -lt ${#liste[@]} ]; do
    echo "Frukt: ${liste[$index]}"
    ((index++))
done
```

## Tips
- Sørg for at betingelsen i `while`-sløyfen vil bli falsk på et tidspunkt for å unngå uendelige sløyfer.
- Bruk `sleep` for å unngå at sløyfen bruker for mye CPU når den venter på en betingelse.
- Test alltid skriptene dine i et sikkert miljø før du kjører dem i produksjon for å unngå utilsiktede konsekvenser.