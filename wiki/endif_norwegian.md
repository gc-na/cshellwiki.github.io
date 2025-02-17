# [Linux] Bash endif bruksområde: Avslutt if-setninger

## Oversikt
`endif`-kommandoen brukes i Bash-skript for å avslutte en if-setning. Den er en del av kontrollstrukturen i skriptspråket, og gir en måte å strukturere betingede operasjoner på.

## Bruk
Grunnleggende syntaks for `endif`-kommandoen er som følger:

```bash
if [ betingelse ]; then
    # kommandoer
fi
```

`endif` er ikke en eksplisitt kommando i Bash, men `fi` brukes for å avslutte en if-setning.

## Vanlige alternativer
Det finnes ingen spesifikke alternativer for `endif`, men det er viktig å forstå hvordan man bruker `if`, `then`, og `fi` i sammenheng.

## Vanlige eksempler

### Eksempel 1: Enkel if-setning
```bash
if [ -f "fil.txt" ]; then
    echo "Fil eksisterer."
fi
```

### Eksempel 2: If-setning med else
```bash
if [ -d "mappe" ]; then
    echo "Mappen eksisterer."
else
    echo "Mappen finnes ikke."
fi
```

### Eksempel 3: If-setning med flere betingelser
```bash
if [ "$tall" -gt 10 ]; then
    echo "Tallet er større enn 10."
elif [ "$tall" -eq 10 ]; then
    echo "Tallet er lik 10."
else
    echo "Tallet er mindre enn 10."
fi
```

## Tips
- Sørg for å alltid avslutte if-setninger med `fi` for å unngå syntaksfeil.
- Bruk innrykk i skriptene dine for bedre lesbarhet, spesielt når du har flere nivåer av betingelser.
- Test skriptene dine grundig for å sikre at betingelsene fungerer som forventet.