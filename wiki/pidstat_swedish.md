# [Linux] Bash pidstat användning: Övervaka processprestanda

## Översikt
Kommandot `pidstat` används för att övervaka och rapportera statistik om processer i ett Linux-system. Det ger detaljerad information om CPU-användning, minnesanvändning och andra resurser för specifika processer, vilket är användbart för systemadministratörer och utvecklare som vill optimera prestanda.

## Användning
Den grundläggande syntaxen för `pidstat` är:

```
pidstat [alternativ] [argument]
```

## Vanliga alternativ
- `-h`: Visar hjälpmeddelande och information om kommandot.
- `-r`: Visar minnesanvändning för processerna.
- `-u`: Visar CPU-användning för processerna.
- `-p <PID>`: Anger en specifik process-ID att övervaka.
- `-t`: Visar statistik för trådar inom processer.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `pidstat`:

1. Visa CPU-användning för alla processer:
   ```bash
   pidstat -u
   ```

2. Visa minnesanvändning för alla processer:
   ```bash
   pidstat -r
   ```

3. Övervaka en specifik process med PID 1234:
   ```bash
   pidstat -p 1234
   ```

4. Visa statistik för trådar inom en process med PID 5678:
   ```bash
   pidstat -t -p 5678
   ```

5. Visa CPU-användning var 2:a sekund:
   ```bash
   pidstat -u 2
   ```

## Tips
- Använd `pidstat` tillsammans med andra verktyg som `grep` för att filtrera specifika processer.
- Kombinera alternativ för att få en mer detaljerad bild av processernas prestanda.
- Tänk på att köra `pidstat` med tillräckliga rättigheter för att få åtkomst till all nödvändig information om processerna.