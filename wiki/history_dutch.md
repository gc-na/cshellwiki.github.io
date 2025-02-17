# [Linux] Bash history gebruik: Geschiedenis van commando's bekijken

## Overzicht
De `history`-opdracht in Bash toont een lijst van eerder ingevoerde commando's. Dit is handig om snel toegang te krijgen tot vaak gebruikte commando's of om te zien wat je eerder hebt gedaan in de terminal.

## Gebruik
De basis syntaxis van de `history`-opdracht is als volgt:

```bash
history [opties] [argumenten]
```

## Veelvoorkomende opties
- `-c`: Wis de geschiedenis.
- `-d <n>`: Verwijder het commando met het nummer `<n>` uit de geschiedenis.
- `-a`: Voeg de huidige geschiedenis toe aan het geschiedenisbestand.
- `-r`: Lees de geschiedenis van het geschiedenisbestand.

## Veelvoorkomende voorbeelden

1. **Bekijk de geschiedenis van commando's:**
   ```bash
   history
   ```

2. **Bekijk de laatste 10 commando's:**
   ```bash
   history 10
   ```

3. **Verwijder een specifiek commando uit de geschiedenis:**
   ```bash
   history -d 5
   ```

4. **Wis de gehele geschiedenis:**
   ```bash
   history -c
   ```

5. **Voeg de huidige geschiedenis toe aan het bestand:**
   ```bash
   history -a
   ```

## Tips
- Gebruik de pijltjestoetsen omhoog en omlaag om door je geschiedenis te bladeren.
- Typ `!n` om het commando met nummer `n` opnieuw uit te voeren.
- Maak gebruik van `Ctrl + R` voor een reverse search in je geschiedenis, wat het vinden van eerder gebruikte commando's vergemakkelijkt.