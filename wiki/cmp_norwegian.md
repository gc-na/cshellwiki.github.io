# [Linux] Bash cmp bruk: Sammenlign to filer byte for byte

## Oversikt
`cmp`-kommandoen brukes til å sammenligne to filer byte for byte. Den viser forskjellene mellom filene, og hvis de er identiske, gir den ingen utdata. Dette verktøyet er nyttig for å sjekke om to filer er like eller for å finne ut hvor de skiller seg fra hverandre.

## Bruk
Den grunnleggende syntaksen for `cmp`-kommandoen er som følger:

```bash
cmp [alternativer] [fil1] [fil2]
```

## Vanlige alternativer
- `-l`: Vis byte-for-byte forskjeller i oktal format.
- `-s`: Still stille, ingen utdata, men returnerer en exit-status.
- `-i OFFSET`: Start sammenligningen fra den angitte byte-offseten.
- `-n N`: Sammenlign bare de første N byte av filene.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `cmp` kan brukes:

### Sammenligne to filer
For å sammenligne to filer og se om de er like eller forskjellige:

```bash
cmp fil1.txt fil2.txt
```

### Sammenligne to filer stille
For å sammenligne to filer uten å vise utdata, men bare få en exit-status:

```bash
cmp -s fil1.txt fil2.txt
```

### Sammenligne spesifikke byte
For å sammenligne bare de første 10 byte av to filer:

```bash
cmp -n 10 fil1.txt fil2.txt
```

### Vise forskjeller i oktal format
For å vise forskjeller mellom to filer i oktal format:

```bash
cmp -l fil1.txt fil2.txt
```

## Tips
- Bruk `-s`-alternativet når du bare er interessert i exit-statusen for å sjekke om filene er like.
- Kombiner `cmp` med `diff` for mer detaljert informasjon om forskjeller mellom filer.
- Husk at `cmp` sammenligner filer byte for byte, så selv små forskjeller vil bli rapportert.