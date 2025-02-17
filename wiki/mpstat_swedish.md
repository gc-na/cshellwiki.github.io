# [Linux] Bash mpstat användning: övervaka CPU-användning

## Översikt
Kommandot `mpstat` används för att visa statistik om CPU-användning på ett system. Det ger detaljerad information om hur mycket av CPU:ns kapacitet som används av olika processer och systemaktiviteter, vilket är användbart för att övervaka prestanda och identifiera flaskhalsar.

## Användning
Den grundläggande syntaxen för kommandot `mpstat` är:

```bash
mpstat [alternativ] [argument]
```

## Vanliga alternativ
- `-P ALL`: Visar statistik för alla CPU:er.
- `-u`: Visar CPU-användning i procent.
- `-h`: Visar resultaten i ett mer läsbart format.
- `interval`: Anger hur ofta (i sekunder) statistiken ska uppdateras.
- `count`: Anger hur många gånger statistiken ska visas.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mpstat`:

1. Visa CPU-användning för alla CPU:er:
   ```bash
   mpstat -P ALL
   ```

2. Visa CPU-användning var 2:a sekund, 5 gånger:
   ```bash
   mpstat 2 5
   ```

3. Visa CPU-användning med ett mer läsbart format:
   ```bash
   mpstat -h
   ```

4. Visa endast användning av system CPU:
   ```bash
   mpstat -u
   ```

## Tips
- Använd `mpstat` tillsammans med andra verktyg som `top` eller `htop` för en mer omfattande övervakning av systemresurser.
- Tänk på att köra `mpstat` med root-privilegier för att få mer detaljerad information om systemets CPU-användning.
- Analysera resultaten över tid för att identifiera mönster i CPU-användning och optimera systemets prestanda.