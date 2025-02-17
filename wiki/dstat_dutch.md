# [Linux] Bash dstat gebruik: systeemmonitoring in real-time

## Overzicht
De `dstat` opdracht is een veelzijdig hulpmiddel voor systeemmonitoring dat real-time informatie biedt over verschillende systeembronnen. Het combineert de functionaliteit van verschillende andere monitoringtools en geeft een overzicht van CPU-, geheugen-, schijf- en netwerkinformatie in een enkele uitvoer.

## Gebruik
De basis syntaxis van de `dstat` opdracht is als volgt:

```bash
dstat [opties] [argumenten]
```

## Veelvoorkomende Opties
Hier zijn enkele veelgebruikte opties voor `dstat`:

- `-c`: Toon CPU-gebruik.
- `-d`: Toon schijfactiviteit.
- `-n`: Toon netwerkactiviteit.
- `-m`: Toon geheugenstatistieken.
- `--full`: Toon alle beschikbare informatie in een uitgebreide weergave.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `dstat`:

1. **Basis gebruik**:
   ```bash
   dstat
   ```
   Dit toont standaard systeemstatistieken zoals CPU, schijf en netwerk.

2. **CPU en geheugen monitoring**:
   ```bash
   dstat -c -m
   ```
   Hiermee worden alleen de CPU- en geheugenstatistieken weergegeven.

3. **Schijf- en netwerkactiviteit**:
   ```bash
   dstat -d -n
   ```
   Dit toont de schijf- en netwerkactiviteit in real-time.

4. **Volledige systeeminformatie**:
   ```bash
   dstat --full
   ```
   Hiermee krijg je een uitgebreide weergave van alle systeemstatistieken.

## Tips
- Gebruik `dstat` met de `-t` optie om tijdstempels aan de uitvoer toe te voegen, wat handig kan zijn voor het analyseren van trends.
- Combineer verschillende opties om een meer gedetailleerd overzicht te krijgen van de systeembronnen die je wilt monitoren.
- Overweeg om `dstat` te gebruiken in combinatie met andere tools zoals `grep` of `awk` voor geavanceerde analyses van de uitvoer.