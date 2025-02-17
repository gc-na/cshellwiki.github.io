# [Linux] Bash sysctl bruk: Justering av kjerneparametere

## Oversikt
`sysctl` er et verktøy i Linux som brukes til å lese og skrive kjerneparametere i sanntid. Dette gjør det mulig for brukere å justere systeminnstillinger uten å måtte starte systemet på nytt.

## Bruk
Den grunnleggende syntaksen for `sysctl` er som følger:

```bash
sysctl [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Viser alle kjerneparametere.
- `-n`: Viser verdien av en spesifisert parameter uten ekstra informasjon.
- `-w`: Endrer verdien av en spesifisert parameter.
- `-p`: Leser inn parametere fra en spesifisert fil.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `sysctl` kan brukes:

1. **Vise alle kjerneparametere:**
   ```bash
   sysctl -a
   ```

2. **Vise verdien av en spesifikk parameter:**
   ```bash
   sysctl -n vm.swappiness
   ```

3. **Endre verdien av en parameter:**
   ```bash
   sysctl -w vm.swappiness=10
   ```

4. **Lese inn kjerneparametere fra en fil:**
   ```bash
   sysctl -p /etc/sysctl.conf
   ```

## Tips
- Vær forsiktig når du endrer kjerneparametere, da feil innstillinger kan påvirke systemets stabilitet.
- Bruk `sysctl -a` for å få en fullstendig oversikt over tilgjengelige parametere og deres nåværende verdier.
- For å gjøre endringer permanente, legg til dem i `/etc/sysctl.conf` og bruk `sysctl -p` for å laste dem inn.