# [Linux] Bash yes gebruik: Herhaal een string eindeloos

## Overzicht
De `yes`-opdracht in Bash is een eenvoudige maar krachtige tool die een opgegeven string of de standaardtekst "y" eindeloos herhaalt. Dit kan handig zijn voor het automatiseren van bevestigingen in scripts of voor het genereren van grote hoeveelheden tekst.

## Gebruik
De basis syntaxis van de `yes`-opdracht is als volgt:

```bash
yes [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`, `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `-V`, `--version`: Toont de versie van de `yes`-opdracht.

## Veelvoorkomende Voorbeelden

1. **Eindeloos "y" herhalen**:
   ```bash
   yes
   ```
   Dit commando herhaalt de letter "y" eindeloos totdat het proces wordt gestopt.

2. **Een specifieke string herhalen**:
   ```bash
   yes "Bevestigen"
   ```
   Dit commando herhaalt de string "Bevestigen" eindeloos.

3. **Bevestigingen doorgeven aan een ander commando**:
   ```bash
   yes | rm -i *.tmp
   ```
   Dit commando gebruikt `yes` om automatisch "y" te sturen naar de `rm` opdracht, waardoor alle tijdelijke bestanden zonder verdere bevestiging worden verwijderd.

4. **Herhalen met een andere string**:
   ```bash
   yes "Ja" | head -n 5
   ```
   Dit commando herhaalt "Ja" en toont alleen de eerste vijf regels.

## Tips
- Gebruik `yes` met voorzichtigheid, vooral in combinatie met destructieve commando's zoals `rm`, om onbedoeld gegevensverlies te voorkomen.
- Combineer `yes` met andere commando's in een pipeline voor efficiënte automatisering.
- Stop de `yes`-opdracht met `Ctrl+C` wanneer je klaar bent met de uitvoer.