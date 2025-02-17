# [Linux] Bash stty gebruik: Instellingen voor terminalinvoer en -uitvoer

## Overzicht
De `stty`-opdracht wordt gebruikt om de instellingen van de terminal te configureren. Hiermee kun je verschillende parameters van de terminal aanpassen, zoals het gedrag van toetsen, het instellen van speciale karakters en het beheren van invoer- en uitvoerinstellingen.

## Gebruik
De basis syntaxis van de `stty`-opdracht is als volgt:

```bash
stty [opties] [argumenten]
```

## Veelvoorkomende opties
- `-a`: Toont alle huidige instellingen van de terminal.
- `-g`: Geeft de huidige instellingen weer in een formaat dat later kan worden hersteld.
- `erase <teken>`: Stelt het teken in dat gebruikt wordt om een teken te wissen.
- `kill <teken>`: Stelt het teken in dat gebruikt wordt om de huidige regel te wissen.
- `intr <teken>`: Stelt het teken in dat gebruikt wordt om een onderbreking te genereren.

## Veelvoorkomende voorbeelden

1. **Toon alle instellingen van de terminal:**
   ```bash
   stty -a
   ```

2. **Stel het wis-teken in op 'Backspace':**
   ```bash
   stty erase ^H
   ```

3. **Stel het onderbrekingsteken in op 'Ctrl+C':**
   ```bash
   stty intr ^C
   ```

4. **Herstel de terminalinstellingen naar een eerder opgeslagen staat:**
   ```bash
   stty $(stty -g)
   ```

5. **Schakel echo uit (geen invoer weergeven):**
   ```bash
   stty -echo
   ```

## Tips
- Gebruik `stty -g` om de huidige instellingen op te slaan voordat je wijzigingen aanbrengt, zodat je deze later kunt herstellen.
- Wees voorzichtig met het uitschakelen van echo, omdat je mogelijk niet kunt zien wat je typt.
- Controleer altijd de instellingen na het aanpassen om er zeker van te zijn dat alles correct is ingesteld.