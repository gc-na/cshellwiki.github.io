# [Linux] Bash env gebruik: Omgevingsvariabelen beheren

## Overzicht
De `env`-opdracht in Bash wordt gebruikt om omgevingsvariabelen te beheren en om programma's met een aangepaste omgeving uit te voeren. Het stelt gebruikers in staat om de huidige omgevingsvariabelen te bekijken of nieuwe omgevingsvariabelen te definiëren voor een specifieke opdracht.

## Gebruik
De basis syntaxis van de `env`-opdracht is als volgt:

```bash
env [opties] [argumenten]
```

## Veelvoorkomende opties
- `-i`: Start een nieuwe omgeving zonder bestaande omgevingsvariabelen.
- `-u VAR`: Verwijdert de opgegeven omgevingsvariabele VAR uit de omgeving.
- `VAR=value`: Definieert een nieuwe omgevingsvariabele VAR met de opgegeven waarde.

## Veelvoorkomende voorbeelden

1. **Weergeven van omgevingsvariabelen**:
   Om alle huidige omgevingsvariabelen weer te geven, gebruik je:
   ```bash
   env
   ```

2. **Een programma uitvoeren met een aangepaste omgevingsvariabele**:
   Om een programma uit te voeren met een specifieke omgevingsvariabele, bijvoorbeeld `MY_VAR`, gebruik je:
   ```bash
   env MY_VAR=waarde mijn_programma
   ```

3. **Een programma uitvoeren zonder bestaande omgevingsvariabelen**:
   Om een programma te starten zonder enige bestaande omgevingsvariabelen, gebruik je:
   ```bash
   env -i mijn_programma
   ```

4. **Verwijderen van een omgevingsvariabele**:
   Om een omgevingsvariabele te verwijderen voordat je een programma uitvoert, gebruik je:
   ```bash
   env -u MY_VAR mijn_programma
   ```

## Tips
- Gebruik `env` om snel omgevingsvariabelen te testen zonder je shell-configuratie aan te passen.
- Het gebruik van `env -i` is handig voor het debuggen van programma's die afhankelijk zijn van specifieke omgevingsvariabelen.
- Vergeet niet dat omgevingsvariabelen hoofdlettergevoelig zijn; `VAR` en `var` worden als verschillende variabelen beschouwd.