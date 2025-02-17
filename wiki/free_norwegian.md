# [Linux] Bash free kommando: Vise minnebruk

## Oversikt
Kommandoen `free` brukes til å vise informasjon om minnebruk på systemet. Den gir en oversikt over tilgjengelig, brukt og buffret minne, samt swap-minne, noe som er nyttig for systemadministrasjon og ytelsesanalyse.

## Bruk
Den grunnleggende syntaksen for `free`-kommandoen er:

```
free [alternativer]
```

## Vanlige alternativer
- `-h`: Viser minneverdier i et lesbart format (f.eks. MB eller GB).
- `-m`: Viser minneverdier i megabyte.
- `-g`: Viser minneverdier i gigabyte.
- `-s <sekunder>`: Oppdaterer visningen med angitt intervall i sekunder.
- `-t`: Viser total minnebruk (både RAM og swap).

## Vanlige eksempler
For å vise minnebruk i et lesbart format:

```bash
free -h
```

For å vise minneverdier i megabyte:

```bash
free -m
```

For å vise minneverdier i gigabyte:

```bash
free -g
```

For å oppdatere visningen hvert 5. sekund:

```bash
free -s 5
```

For å inkludere total minnebruk:

```bash
free -h -t
```

## Tips
- Bruk `free -h` for en rask og lettfattelig oversikt over minnebruken.
- Kombiner `free` med `watch` for kontinuerlig overvåking av minnebruk: 

```bash
watch free -h
```

- Vær oppmerksom på at `free` viser minnebruk i sanntid, så det kan være nyttig å bruke det sammen med andre systemovervåkingsverktøy for en mer omfattende analyse.