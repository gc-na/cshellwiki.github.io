# [Linux] Bash who bruksområde: Vise innloggede brukere

## Oversikt
`who`-kommandoen brukes til å vise en liste over brukere som er innlogget på systemet. Den gir informasjon om brukernavn, terminal, innloggingstidspunkt og mer. Dette kan være nyttig for systemadministratorer og brukere som ønsker å se hvem som er aktive på systemet.

## Bruk
Grunnleggende syntaks for `who`-kommandoen er som følger:

```bash
who [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Viser all tilgjengelig informasjon om innloggede brukere.
- `-b`: Viser tidspunktet for siste systemoppstart.
- `-q`: Viser kun brukernavnene til innloggede brukere og antallet dem.
- `--help`: Viser hjelp for kommandoen.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `who` kan brukes:

1. **Vis alle innloggede brukere:**
   ```bash
   who
   ```

2. **Vis all informasjon om innloggede brukere:**
   ```bash
   who -a
   ```

3. **Vis tidspunktet for siste systemoppstart:**
   ```bash
   who -b
   ```

4. **Vis kun brukernavnene til innloggede brukere:**
   ```bash
   who -q
   ```

## Tips
- Bruk `who` sammen med `wc -l` for å telle antall innloggede brukere:
  ```bash
  who | wc -l
  ```
- For mer detaljert informasjon om en spesifikk bruker, kan du kombinere `who` med `grep`:
  ```bash
  who | grep brukernavn
  ```
- Husk at `who` viser informasjon basert på systemets nåværende tilstand, så resultatene kan endres raskt.