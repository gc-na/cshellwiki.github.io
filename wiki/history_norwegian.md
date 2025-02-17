# [Linux] Bash history bruk: Vise tidligere kommandoer

## Oversikt
Kommandoen `history` i Bash brukes til å vise en liste over tidligere utførte kommandoer i terminalen. Dette kan være nyttig for å repetere eller referere til tidligere arbeid uten å måtte skrive inn kommandoene på nytt.

## Bruk
Den grunnleggende syntaksen for `history`-kommandoen er som følger:

```bash
history [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c`: Tømmer historikken.
- `-d offset`: Sletter kommandoen på den spesifiserte posisjonen i historikken.
- `n`: Viser de siste n kommandoene fra historikken.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `history`-kommandoen:

1. **Vis hele historikken:**
   ```bash
   history
   ```

2. **Vis de siste 10 kommandoene:**
   ```bash
   history 10
   ```

3. **Slett en spesifikk kommando fra historikken:**
   ```bash
   history -d 5
   ```

4. **Tøm hele historikken:**
   ```bash
   history -c
   ```

## Tips
- Bruk `!n` for å kjøre kommandoen på linje n i historikken. For eksempel, `!42` vil kjøre kommandoen som er på linje 42.
- Du kan søke i historikken ved å bruke `Ctrl + r` og begynne å skrive en del av kommandoen.
- Vær oppmerksom på at historikken kan inneholde sensitive data, så vær forsiktig med hva som lagres.