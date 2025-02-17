# [Linux] Bash vmstat Bruk: Viser systemytelse

## Oversikt
`vmstat` (virtuell minne statistikk) er et kommandolinjeverktøy som gir informasjon om systemets minne, prosessering, inn- og utdata, samt systemets CPU-aktivitet. Det hjelper brukere med å overvåke systemytelsen og identifisere flaskehalser.

## Bruk
Grunnleggende syntaks for `vmstat`-kommandoen er:

```bash
vmstat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Viser aktivt og inaktivt minne.
- `-m`: Viser minnebruken for cache og buffer.
- `-s`: Viser en oppsummering av minnestatistikk.
- `-t`: Viser tidsstempel for hver rad med utdata.
- `delay`: Angir hvor ofte (i sekunder) informasjonen skal oppdateres.
- `count`: Angir hvor mange ganger informasjonen skal oppdateres.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `vmstat`:

1. Vise systemytelse med standardinnstillinger:
   ```bash
   vmstat
   ```

2. Vise minnestatistikk med oppdatering hvert 2. sekund:
   ```bash
   vmstat 2
   ```

3. Vise minnebruk med detaljer om aktivt og inaktivt minne:
   ```bash
   vmstat -a
   ```

4. Vise en oppsummering av minnestatistikk:
   ```bash
   vmstat -s
   ```

5. Vise systemytelse med tidsstempel:
   ```bash
   vmstat -t 1 5
   ```

## Tips
- Bruk `vmstat` sammen med andre verktøy som `top` eller `htop` for en mer omfattende analyse av systemytelsen.
- Overvåk systemet over tid ved å bruke `vmstat` med `delay` og `count` for å se trender i minne- og CPU-bruk.
- Vær oppmerksom på at `vmstat` viser gjennomsnittlige verdier, så det kan være nyttig å kombinere med mer detaljerte verktøy for spesifikke analyser.