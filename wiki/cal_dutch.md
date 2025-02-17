# [Linux] Bash cal gebruik: Toont een kalender

## Overzicht
De `cal`-opdracht in Bash is een eenvoudige manier om een kalender weer te geven in de terminal. Het kan worden gebruikt om de kalender van een specifieke maand of jaar te tonen, en het biedt ook de mogelijkheid om de huidige maand of een aangepaste maand weer te geven.

## Gebruik
De basis syntaxis van de `cal`-opdracht is als volgt:

```bash
cal [opties] [argumenten]
```

## Veelvoorkomende opties
- `-m`: Toont de kalender van de huidige maand.
- `-y`: Toont de kalender van het huidige jaar.
- `-3`: Toont de kalender van de vorige maand, de huidige maand en de volgende maand.
- `-j`: Toont de dagen van het jaar in plaats van de weken.
- `-A [n]`: Toont de kalender van de volgende `n` maanden.
- `-B [n]`: Toont de kalender van de vorige `n` maanden.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `cal`-opdracht:

1. **Toon de kalender van de huidige maand:**
   ```bash
   cal
   ```

2. **Toon de kalender van een specifieke maand en jaar (bijvoorbeeld maart 2023):**
   ```bash
   cal 03 2023
   ```

3. **Toon de kalender van het huidige jaar:**
   ```bash
   cal -y
   ```

4. **Toon de kalender van de vorige, huidige en volgende maand:**
   ```bash
   cal -3
   ```

5. **Toon de kalender van de volgende 3 maanden:**
   ```bash
   cal -A 3
   ```

## Tips
- Gebruik de optie `-j` als je geïnteresseerd bent in de dagen van het jaar, wat handig kan zijn voor planningen.
- Combineer opties voor meer flexibiliteit, bijvoorbeeld `cal -A 1 -B 1` om de kalenders van de vorige en volgende maand te bekijken.
- Vergeet niet dat je ook specifieke jaren kunt opgeven om historische kalenders te bekijken.