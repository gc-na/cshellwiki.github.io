# [Linux] Bash cal bruksområde: Vise kalendere

## Oversikt
`cal`-kommandoen brukes til å vise en kalender i terminalen. Den gir en enkel og rask måte å se månedlige eller årlige kalendere på, noe som kan være nyttig for planlegging og organisering.

## Bruk
Grunnleggende syntaks for `cal`-kommandoen er:

```bash
cal [alternativer] [argumenter]
```

## Vanlige alternativer
- `-m`: Viser måneden i dag.
- `-y`: Viser hele året.
- `-3`: Viser den nåværende måneden, samt måneden før og etter.
- `-j`: Viser dagene i året (Julian kalender).
- `-A [num]`: Viser de neste [num] månedene.
- `-B [num]`: Viser de forrige [num] månedene.

## Vanlige eksempler
For å vise den nåværende måneden:

```bash
cal
```

For å vise hele året 2023:

```bash
cal 2023
```

For å vise kalenderen for mars 2024:

```bash
cal 03 2024
```

For å vise den nåværende måneden sammen med måneden før og etter:

```bash
cal -3
```

For å vise kalenderen med julian dager:

```bash
cal -j
```

## Tips
- Bruk `cal -y` for raskt å få oversikt over hele året.
- Kombiner alternativer, for eksempel `cal -A 2 -B 1` for å vise to fremtidige måneder og en tidligere måned.
- For en mer visuell fremstilling, kan du bruke `ncal`-kommandoen, som gir en annen layout av kalenderen.