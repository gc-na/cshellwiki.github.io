# [Linux] Bash journalctl Bruk: Vise systemlogger

## Oversikt
`journalctl` er et verktøy som brukes for å vise og administrere systemlogger på systemer som bruker systemd. Det gir en enkel måte å få tilgang til loggmeldinger fra forskjellige tjenester og systemkomponenter, noe som er nyttig for feilsøking og overvåking av systemet.

## Bruk
Grunnleggende syntaks for `journalctl` er som følger:

```bash
journalctl [alternativer] [argumenter]
```

## Vanlige alternativer
- `-b` : Viser logger fra den siste oppstarten.
- `-f` : Følg med på loggene i sanntid (som `tail -f`).
- `--since` : Viser logger fra et spesifisert tidspunkt.
- `--until` : Viser logger frem til et spesifisert tidspunkt.
- `-u <tjeneste>` : Viser logger for en spesifikk systemd-tjeneste.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `journalctl`:

1. **Vise alle logger:**
   ```bash
   journalctl
   ```

2. **Vise logger fra den siste oppstarten:**
   ```bash
   journalctl -b
   ```

3. **Følge med på loggene i sanntid:**
   ```bash
   journalctl -f
   ```

4. **Vise logger fra en spesifikk tjeneste:**
   ```bash
   journalctl -u nginx.service
   ```

5. **Vise logger fra et spesifisert tidspunkt:**
   ```bash
   journalctl --since "2023-10-01 10:00:00" --until "2023-10-01 12:00:00"
   ```

## Tips
- Bruk `-p` for å filtrere logger etter alvorlighetsgrad (f.eks. `-p err` for å vise bare feil).
- Kombiner alternativer for mer spesifikke søk, som `journalctl -u <tjeneste> -b`.
- Lagre logger til en fil ved å bruke omdirigering: 
  ```bash
  journalctl > loggfil.txt
  ```