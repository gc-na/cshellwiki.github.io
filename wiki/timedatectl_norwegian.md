# [Linux] Bash timedatectl bruk: Administrer tid og dato

## Oversikt
`timedatectl` er et kommandolinjeverktøy som brukes til å vise og endre systemets tid og dato, samt tilpasse tidssoneinnstillinger. Det er en del av systemd og gir en enkel måte å håndtere tid og dato på Linux-baserte systemer.

## Bruk
Grunnleggende syntaks for `timedatectl` er som følger:

```bash
timedatectl [alternativer] [argumenter]
```

## Vanlige alternativer
- `status`: Viser den nåværende tid, dato og tidssoneinnstillinger.
- `set-time`: Setter systemets tid og dato.
- `set-timezone`: Endrer systemets tidssone.
- `set-ntp`: Aktiverer eller deaktiverer NTP (Network Time Protocol) synkronisering.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `timedatectl`:

1. **Vis nåværende tid og dato:**
   ```bash
   timedatectl status
   ```

2. **Sett systemets tid og dato:**
   ```bash
   timedatectl set-time '2023-10-01 12:00:00'
   ```

3. **Endre tidssone til Europe/Oslo:**
   ```bash
   timedatectl set-timezone Europe/Oslo
   ```

4. **Aktiver NTP-synkronisering:**
   ```bash
   timedatectl set-ntp true
   ```

5. **Deaktiver NTP-synkronisering:**
   ```bash
   timedatectl set-ntp false
   ```

## Tips
- Sørg for at du har nødvendige rettigheter (som root) for å endre tid og dato.
- Bruk `timedatectl list-timezones` for å se en liste over tilgjengelige tidssoner før du endrer tidssonen.
- Kontroller alltid systemklokken etter endringer for å sikre at alt er korrekt innstilt.