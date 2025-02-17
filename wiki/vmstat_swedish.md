# [Linux] Bash vmstat användning: Övervaka systemresurser

## Översikt
`vmstat` är ett kommandoradsverktyg som används för att övervaka systemets resurser, inklusive minnesanvändning, processer, in- och utmatning samt systembelastning. Det ger en översiktlig bild av systemets prestanda och kan hjälpa till att identifiera flaskhalsar.

## Användning
Den grundläggande syntaxen för `vmstat` är:

```bash
vmstat [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Visar aktivt och inaktivt minne.
- `-m`: Visar minnesstatistik för slab-allokatorn.
- `-s`: Visar sammanfattad minnesstatistik.
- `-d`: Visar diskstatistik.
- `interval`: Anger hur ofta (i sekunder) statistiken ska uppdateras.
- `count`: Anger hur många gånger statistiken ska visas.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `vmstat`:

1. Visa systemstatistik en gång:
   ```bash
   vmstat
   ```

2. Visa systemstatistik var 2:a sekund:
   ```bash
   vmstat 2
   ```

3. Visa systemstatistik var 5:e sekund, 10 gånger:
   ```bash
   vmstat 5 10
   ```

4. Visa minnesstatistik:
   ```bash
   vmstat -a
   ```

5. Visa diskstatistik:
   ```bash
   vmstat -d
   ```

## Tips
- Använd `vmstat` i kombination med andra verktyg som `top` eller `htop` för en mer detaljerad analys av systemets prestanda.
- Titta på kolumnerna för "si" (swap in) och "so" (swap out) för att identifiera potentiella minnesproblem.
- Om du övervakar ett system under en längre tid, överväg att logga utdata till en fil för senare analys.