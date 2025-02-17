# [Linux] Bash watch gebruik: Voortdurend een commando uitvoeren

## Overzicht
De `watch`-opdracht in Bash stelt gebruikers in staat om een bepaald commando op regelmatige tijdstippen uit te voeren en de uitvoer in real-time te bekijken. Dit is bijzonder handig voor het monitoren van veranderingen in de uitvoer van een commando, zoals systeemstatistieken of logbestanden.

## Gebruik
De basis syntaxis van de `watch`-opdracht is als volgt:

```bash
watch [opties] [commando]
```

## Veelvoorkomende Opties
- `-n, --interval`: Stel het interval in seconden in tussen de uitvoeringen van het commando. Standaard is dit 2 seconden.
- `-d, --differences`: Markeer de verschillen tussen de huidige en de vorige uitvoer.
- `-t, --no-title`: Verberg de titelbalk met informatie over het commando en het interval.
- `-x, --exec`: Voer een commando uit met argumenten.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `watch`-opdracht:

1. **Systeembronnen controleren:**
   Om de CPU-gebruik in real-time te volgen, gebruik je:
   ```bash
   watch -n 1 mpstat
   ```

2. **Bestandssysteemgebruik monitoren:**
   Om het gebruik van schijfruimte elke 5 seconden te controleren:
   ```bash
   watch -n 5 df -h
   ```

3. **Netwerkverbindingen volgen:**
   Om actieve netwerkverbindingen te bekijken:
   ```bash
   watch -n 2 netstat -tuln
   ```

4. **Logbestanden in de gaten houden:**
   Om de laatste regels van een logbestand te volgen:
   ```bash
   watch tail -n 10 /var/log/syslog
   ```

## Tips
- Gebruik de `-d` optie om snel veranderingen in de uitvoer te identificeren, wat handig kan zijn bij het monitoren van logbestanden of systeemstatistieken.
- Pas het interval aan met de `-n` optie om de belasting op het systeem te minimaliseren, vooral bij commando's die veel middelen vereisen.
- Combineer `watch` met andere commando's zoals `grep` om specifieke informatie te filteren en alleen relevante uitvoer te tonen.