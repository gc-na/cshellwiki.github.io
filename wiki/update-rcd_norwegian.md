# [Linux] Bash update-rc.d Bruk: Legge til eller fjerne tjenester fra oppstart

## Oversikt
`update-rc.d` er et Bash-kommando som brukes til å legge til, fjerne eller oppdatere oppstartstjenester i Linux-systemer. Den håndterer oppstartsskript som finnes i `/etc/init.d/` og oppdaterer de nødvendige symlinkene i `/etc/rc*.d/` katalogene for å kontrollere når og hvordan tjenester startes og stoppes under systemoppstart.

## Bruk
Grunnleggende syntaks for `update-rc.d`-kommandoen er som følger:

```bash
update-rc.d [alternativer] [argumenter]
```

## Vanlige alternativer
- `defaults`: Legger til tjenesten med standard oppstartsnivåer.
- `remove`: Fjerner tjenesten fra oppstart.
- `enable`: Aktiverer tjenesten for oppstart.
- `disable`: Deaktiverer tjenesten fra oppstart.
- `force`: Tvinger oppdatering av symlinker, selv om det kan være risiko for konflikter.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `update-rc.d`:

1. **Legge til en tjeneste med standardinnstillinger:**
   ```bash
   sudo update-rc.d myservice defaults
   ```

2. **Fjerne en tjeneste fra oppstart:**
   ```bash
   sudo update-rc.d myservice remove
   ```

3. **Aktivere en tjeneste for oppstart:**
   ```bash
   sudo update-rc.d myservice enable
   ```

4. **Deaktivere en tjeneste fra oppstart:**
   ```bash
   sudo update-rc.d myservice disable
   ```

5. **Tvinge oppdatering av symlinker:**
   ```bash
   sudo update-rc.d myservice defaults force
   ```

## Tips
- Sørg for å bruke `sudo` når du kjører `update-rc.d`, ettersom det krever administrative rettigheter.
- Kontroller alltid at tjenesten har et korrekt oppstartsskript i `/etc/init.d/` før du prøver å legge den til oppstart.
- Bruk `update-rc.d` med forsiktighet, spesielt med `force`-alternativet, for å unngå utilsiktede endringer i systemets oppstart.
- Etter endringer, kan du bruke `service myservice status` for å sjekke om tjenesten er aktivert som forventet.