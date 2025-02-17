# [Linux] Bash fg gebruik: Brengt een achtergrondtaak naar de voorgrond

## Overzicht
De `fg` (foreground) opdracht in Bash wordt gebruikt om een achtergrondtaak naar de voorgrond te brengen. Dit is handig wanneer je een proces hebt gestart in de achtergrond en je wilt het weer actief maken zodat je ermee kunt interageren.

## Gebruik
De basis syntaxis van de `fg` opdracht is als volgt:

```bash
fg [opties] [argumenten]
```

## Veelvoorkomende Opties
- `job_spec`: Hiermee geef je de specifieke taak aan die je naar de voorgrond wilt brengen. Dit kan een jobnummer of een proces-ID zijn.
- `+`: Brengt de meest recente achtergrondtaak naar de voorgrond.
- `-`: Brengt de op één na meest recente achtergrondtaak naar de voorgrond.

## Veelvoorkomende Voorbeelden

1. **Breng de meest recente achtergrondtaak naar de voorgrond:**
   ```bash
   fg
   ```

2. **Breng een specifieke taak naar de voorgrond met jobnummer 1:**
   ```bash
   fg %1
   ```

3. **Breng de op één na meest recente taak naar de voorgrond:**
   ```bash
   fg -
   ```

4. **Breng een taak naar de voorgrond met een specifieke proces-ID (PID):**
   ```bash
   fg %1234
   ```

## Tips
- Zorg ervoor dat je de juiste job of PID gebruikt om verwarring te voorkomen.
- Gebruik de `jobs` opdracht om een lijst van actieve achtergrondtaken te bekijken voordat je `fg` gebruikt.
- Als je een taak naar de voorgrond brengt, kun je deze onderbreken met `Ctrl + Z` om het naar de achtergrond te verplaatsen, of `Ctrl + C` om het te beëindigen.