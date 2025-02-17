# [Linux] Bash last gebruik: Toon inloggeschiedenis

## Overzicht
De `last` opdracht in Bash toont de inloggeschiedenis van gebruikers op het systeem. Het geeft een lijst weer van gebruikers die zich hebben aangemeld, samen met de tijdstippen van inloggen en uitloggen.

## Gebruik
De basis syntaxis van de `last` opdracht is als volgt:

```bash
last [opties] [argumenten]
```

## Veelvoorkomende opties
- `-a`: Toont het hostname of het IP-adres van de gebruiker.
- `-n [aantal]`: Beperk het aantal weergegeven inlogrecords tot het opgegeven aantal.
- `-x`: Toont ook systeemopdrachten zoals reboot en shutdown.

## Veelvoorkomende voorbeelden

1. **Toon de laatste inloggeschiedenis van alle gebruikers:**
   ```bash
   last
   ```

2. **Toon de laatste 5 inlogrecords:**
   ```bash
   last -n 5
   ```

3. **Toon inloggeschiedenis met hostnamen:**
   ```bash
   last -a
   ```

4. **Toon ook systeemopdrachten:**
   ```bash
   last -x
   ```

5. **Toon inloggeschiedenis van een specifieke gebruiker:**
   ```bash
   last username
   ```

## Tips
- Gebruik de `-n` optie om de output te beperken tot een beheersbaar aantal records, vooral op systemen met veel gebruikersactiviteit.
- Combineer de `-a` en `-x` opties voor een uitgebreid overzicht van zowel gebruikers als systeemactiviteiten.
- Controleer regelmatig de inloggeschiedenis om ongebruikelijke activiteiten te detecteren en de beveiliging van je systeem te waarborgen.