# [Linux] Bash ved at: Planlegg oppgaver for senere kjøring

## Oversikt
`at`-kommandoen brukes til å planlegge oppgaver som skal kjøres på et spesifisert tidspunkt i fremtiden. Dette er nyttig for å automatisere oppgaver som ikke trenger å kjøres umiddelbart.

## Bruk
Grunnleggende syntaks for `at`-kommandoen er som følger:

```bash
at [alternativer] [argumenter]
```

## Vanlige alternativer
- `-f` : Angi en fil som inneholder kommandoene som skal kjøres.
- `-m` : Send en e-post når oppgaven er fullført.
- `-q` : Angi en kø for oppgaven.
- `-l` : List opp alle planlagte oppgaver.
- `-d` : Slett en planlagt oppgave.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `at`-kommandoen kan brukes:

1. **Planlegge en enkel oppgave:**
   Kjør en skriptfil kl. 15:00 i dag.
   ```bash
   echo "/path/to/script.sh" | at 15:00
   ```

2. **Planlegge en oppgave for i morgen:**
   Kjør en kommando i morgen kl. 10:00.
   ```bash
   echo "backup.sh" | at 10:00 tomorrow
   ```

3. **Bruke en fil med kommandoer:**
   Kjør kommandoene som er lagret i en fil kl. 18:00.
   ```bash
   at -f /path/to/commands.txt 18:00
   ```

4. **Liste opp planlagte oppgaver:**
   Se alle oppgaver som er planlagt.
   ```bash
   at -l
   ```

5. **Slette en planlagt oppgave:**
   Slett en oppgave med jobbenummer 2.
   ```bash
   at -d 2
   ```

## Tips
- Sørg for at `atd`-tjenesten kjører på systemet ditt for at planlagte oppgaver skal fungere.
- Bruk `at -m` for å motta e-post når oppgaven er fullført, slik at du kan bekrefte at den har blitt utført.
- Planlegg oppgaver i god tid for å unngå konflikter med andre oppgaver som kan kjøre samtidig.