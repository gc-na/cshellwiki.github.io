# [Linux] Bash iostat gebruik: Monitoren van systeeminvoer- en uitvoeractiviteit

## Overzicht
De `iostat`-opdracht is een hulpmiddel dat wordt gebruikt om statistieken over systeeminvoer- en uitvoeractiviteit te verzamelen en weer te geven. Het biedt informatie over de prestaties van de schijf en de CPU, wat nuttig is voor het diagnosticeren van prestatieproblemen en het optimaliseren van systeembronnen.

## Gebruik
De basisstructuur van de `iostat`-opdracht is als volgt:

```bash
iostat [opties] [argumenten]
```

## Veelvoorkomende opties
- `-c`: Toont alleen CPU-statistieken.
- `-d`: Toont alleen schijfstatistieken.
- `-x`: Toont uitgebreide schijfstatistieken.
- `-h`: Toont de uitvoer in een leesbaar formaat (bijvoorbeeld in kilobytes of megabytes).
- `interval`: De tijd in seconden tussen de rapportages.
- `count`: Het aantal rapportages dat moet worden weergegeven.

## Veelvoorkomende voorbeelden

1. **Basisgebruik zonder opties**:
   ```bash
   iostat
   ```

2. **Toon alleen CPU-statistieken**:
   ```bash
   iostat -c
   ```

3. **Toon schijfstatistieken met uitgebreide informatie**:
   ```bash
   iostat -x
   ```

4. **Rapportage elke 5 seconden, 3 keer**:
   ```bash
   iostat 5 3
   ```

5. **Toon schijfstatistieken in een leesbaar formaat**:
   ```bash
   iostat -d -h
   ```

## Tips
- Gebruik de `-x` optie voor gedetailleerdere schijfstatistieken, vooral als je vermoedt dat er prestatieproblemen zijn.
- Combineer `iostat` met andere monitoringtools zoals `top` of `vmstat` voor een completer beeld van de systeemprestaties.
- Houd rekening met de frequentie van rapportages; te vaak rapporteren kan zelf een belasting voor het systeem zijn.