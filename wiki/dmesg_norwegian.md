# [Linux] Bash dmesg bruk: Vise kjernemeldinger

## Oversikt
`dmesg`-kommandoen brukes til å vise meldinger fra kjernen i Linux-operativsystemet. Den gir informasjon om systemoppstart, maskinvare og enhetsdrivere, og kan være nyttig for feilsøking av systemproblemer.

## Bruk
Grunnleggende syntaks for `dmesg`-kommandoen er som følger:

```bash
dmesg [alternativer] [argumenter]
```

## Vanlige alternativer
- `-C` : Tøm dmesg-bufferen.
- `-c` : Tøm dmesg-bufferen og vis innholdet.
- `-n level` : Sett nivået for meldinger som skal vises.
- `-T` : Vis tidsstempler i menneskelig lesbar form.
- `--help` : Vis hjelp for dmesg-kommandoen.

## Vanlige eksempler
For å vise alle kjernemeldinger:

```bash
dmesg
```

For å vise kjernemeldinger med tidsstempler:

```bash
dmesg -T
```

For å tømme dmesg-bufferen og vise innholdet:

```bash
dmesg -c
```

For å vise meldinger med et spesifikt nivå (for eksempel nivå 3):

```bash
dmesg -n 3
```

## Tips
- Bruk `dmesg | less` for å bla gjennom lange meldinger.
- Kombiner `dmesg` med `grep` for å filtrere spesifikke meldinger, for eksempel:

```bash
dmesg | grep error
```

- Vær oppmerksom på at dmesg-meldinger kan gi verdifull informasjon for feilsøking av maskinvareproblemer.