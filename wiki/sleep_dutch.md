# [Linux] Bash sleep gebruik: Pauzeert de uitvoering van een script

## Overzicht
De `sleep` opdracht in Bash wordt gebruikt om de uitvoering van een script of commando voor een bepaalde periode te pauzeren. Dit kan handig zijn in verschillende situaties, zoals het wachten op een proces of het creëren van vertragingen in een script.

## Gebruik
De basis syntaxis van de `sleep` opdracht is als volgt:

```
sleep [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`, `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `-v`, `--version`: Toont de versie van de `sleep` opdracht.

## Veelvoorkomende Voorbeelden

1. **Pauzeer voor 5 seconden:**
   ```bash
   sleep 5
   ```

2. **Pauzeer voor 2 minuten:**
   ```bash
   sleep 2m
   ```

3. **Pauzeer voor 1 uur:**
   ```bash
   sleep 1h
   ```

4. **Pauzeer voor 10 seconden en voer daarna een commando uit:**
   ```bash
   sleep 10 && echo "10 seconden gewacht"
   ```

5. **Pauzeer voor een variabele tijd:**
   ```bash
   tijd=3
   sleep $tijd
   ```

## Tips
- Gebruik `sleep` in scripts om de uitvoering te synchroniseren met externe processen of om een wachttijd in te bouwen.
- Combineer `sleep` met andere commando's om een betere controle over de uitvoeringstijd van taken te krijgen.
- Houd rekening met de tijdseenheden: je kunt seconden, minuten (m), uren (h) en dagen (d) gebruiken.