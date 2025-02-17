# [Linux] Bash jobs gebruik: Beheer achtergrondprocessen

## Overzicht
De `jobs`-opdracht in Bash wordt gebruikt om een lijst van de actieve achtergrondprocessen van de huidige shell weer te geven. Dit is handig om te zien welke taken op de achtergrond draaien en om hun status te controleren.

## Gebruik
De basis syntaxis van de `jobs`-opdracht is als volgt:

```bash
jobs [opties] [argumenten]
```

## Veelvoorkomende opties
- `-l`: Toont de PID (Process ID) van elk proces.
- `-n`: Toont alleen de jobs die recentelijk zijn gewijzigd.
- `-p`: Toont alleen de PID's van de jobs.

## Veelvoorkomende voorbeelden

1. **Basis gebruik**: Lijst alle achtergrondprocessen.
   ```bash
   jobs
   ```

2. **Lijst met PID's**: Toon de achtergrondprocessen met hun PID's.
   ```bash
   jobs -l
   ```

3. **Recent gewijzigde jobs**: Toon alleen de jobs die recent zijn gewijzigd.
   ```bash
   jobs -n
   ```

4. **PID's van jobs**: Verkrijg alleen de PID's van de achtergrondprocessen.
   ```bash
   jobs -p
   ```

## Tips
- Gebruik `bg` om een job die op de achtergrond draait opnieuw te starten als deze is gepauzeerd.
- Met `fg` kun je een achtergrondjob naar de voorgrond brengen.
- Controleer regelmatig je achtergrondprocessen om te voorkomen dat je belangrijke taken uit het oog verliest.