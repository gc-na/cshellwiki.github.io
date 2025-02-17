# [Linux] Bash nice gebruik: Beheer de prioriteit van processen

## Overzicht
De `nice` opdracht in Bash wordt gebruikt om de prioriteit van processen te beheren. Hiermee kun je de CPU-tijd die aan een proces wordt toegewezen, verhogen of verlagen, waardoor je de prestaties van je systeem kunt optimaliseren.

## Gebruik
De basis syntaxis van de `nice` opdracht is als volgt:

```bash
nice [opties] [commando] [argumenten]
```

## Veelvoorkomende Opties
- `-n`, `--adjustment`: Hiermee kun je de prioriteit van het proces aanpassen. Een positieve waarde verlaagt de prioriteit, terwijl een negatieve waarde deze verhoogt.
- `-h`, `--help`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `-v`, `--version`: Toont de versie van de `nice` opdracht.

## Veelvoorkomende Voorbeelden

1. **Een proces met standaard prioriteit starten:**
   ```bash
   nice sleep 10
   ```
   Dit start het `sleep` commando met de standaard prioriteit.

2. **Een proces met verhoogde prioriteit starten:**
   ```bash
   nice -n -5 make
   ```
   Dit start het `make` commando met een hogere prioriteit, wat betekent dat het meer CPU-tijd krijgt.

3. **Een proces met verlaagde prioriteit starten:**
   ```bash
   nice -n 10 gzip bestand.txt
   ```
   Dit start het `gzip` commando met een lagere prioriteit, zodat andere processen meer CPU-tijd kunnen krijgen.

4. **De prioriteit van een bestaand proces wijzigen:**
   ```bash
   renice -n 5 -p 1234
   ```
   Dit wijzigt de prioriteit van het proces met PID 1234 naar een lagere prioriteit.

## Tips
- Gebruik `nice` voor achtergrondprocessen die niet veel CPU-tijd nodig hebben, zodat je systeem responsief blijft.
- Controleer de huidige prioriteit van processen met de `top` of `htop` commando's.
- Wees voorzichtig met het verhogen van de prioriteit van processen, omdat dit andere belangrijke processen kan beïnvloeden.