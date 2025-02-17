# [Linux] Bash stty bruk: Konfigurer terminalinnstillinger

## Oversikt
`stty` er et Bash-kommando som brukes til å endre og vise terminalinnstillinger. Den gir brukeren mulighet til å tilpasse hvordan terminalen håndterer input og output, noe som kan være nyttig for å forbedre brukeropplevelsen i kommandolinjemiljøer.

## Bruk
Grunnleggende syntaks for `stty`-kommandoen er som følger:

```bash
stty [alternativer] [argumenter]
```

## Vanlige alternativer
- `-a`: Viser alle innstillinger for terminalen.
- `-g`: Viser innstillingene i en form som kan brukes med `stty` for å gjenopprette dem senere.
- `erase`: Setter tegn for sletting av siste tegn (backspace).
- `kill`: Setter tegn for å slette hele linjen.
- `intr`: Setter tegn for avbrytelse av prosesser (vanligvis Ctrl+C).

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `stty` kan brukes:

1. **Vise nåværende terminalinnstillinger:**
   ```bash
   stty -a
   ```

2. **Endre backspace-tasten til å fungere som forventet:**
   ```bash
   stty erase ^H
   ```

3. **Sett Ctrl+C som avbrytelsestegn:**
   ```bash
   stty intr ^C
   ```

4. **Lagre nåværende innstillinger for senere gjenoppretting:**
   ```bash
   stty -g > innstillinger.txt
   ```

5. **Gjenopprette innstillinger fra en fil:**
   ```bash
   stty $(<innstillinger.txt)
   ```

## Tips
- Vær forsiktig når du endrer terminalinnstillinger, da feil innstillinger kan gjøre terminalen vanskelig å bruke.
- Bruk `stty -g` for å lagre innstillinger før du gjør endringer, slik at du enkelt kan gjenopprette dem.
- Test innstillingene i et trygt miljø før du bruker dem i produksjon for å unngå uventede problemer.