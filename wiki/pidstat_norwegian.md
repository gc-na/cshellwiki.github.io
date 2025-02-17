# [Linux] Bash pidstat Bruk: Overvåk prosessytelse

## Oversikt
`pidstat` er et verktøy i Linux som brukes til å overvåke og rapportere prosessytelse. Det gir detaljerte statistikker om CPU-bruk, minnebruk og andre ressurser for spesifikke prosesser, noe som er nyttig for systemadministrasjon og feilsøking.

## Bruk
Grunnleggende syntaks for `pidstat`-kommandoen er som følger:

```bash
pidstat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-h`: Viser overskrifter for kolonnene.
- `-r`: Viser minnebruk for prosesser.
- `-u`: Viser CPU-bruk for prosesser.
- `-p <pid>`: Angir spesifikke prosess-IDer for overvåking.
- `-t`: Viser tråder i tillegg til prosesser.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `pidstat`:

1. **Overvåke CPU-bruk for alle prosesser:**
   ```bash
   pidstat -u 1
   ```
   Dette vil vise CPU-bruken for alle prosesser hvert sekund.

2. **Overvåke minnebruk for en spesifikk prosess:**
   ```bash
   pidstat -r -p 1234 1
   ```
   Her overvåkes minnebruken for prosessen med PID 1234 hvert sekund.

3. **Vise både CPU- og minnebruk:**
   ```bash
   pidstat -u -r 1
   ```
   Dette gir en oversikt over både CPU- og minnebruk for alle prosesser hvert sekund.

4. **Overvåke spesifikke prosesser:**
   ```bash
   pidstat -p 1234,5678 1
   ```
   Her overvåkes prosessene med PID 1234 og 5678 hvert sekund.

## Tips
- Bruk `-h` for å få en bedre oversikt over kolonnene og dataene som vises.
- Kombiner `pidstat` med andre verktøy som `grep` for å filtrere resultater basert på spesifikke prosesser.
- Vær oppmerksom på at hyppig overvåking kan påvirke systemytelsen, så tilpass intervallene etter behov.