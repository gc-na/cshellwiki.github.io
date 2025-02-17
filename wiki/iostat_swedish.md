# [Linux] Bash iostat användning: Övervaka systemets I/O-prestanda

## Översikt
Kommandot `iostat` används för att övervaka och rapportera systemets in- och utdata (I/O) prestanda. Det ger information om CPU-användning och I/O-statistik för blockenheter, vilket hjälper administratörer att identifiera flaskhalsar och optimera systemets prestanda.

## Användning
Den grundläggande syntaxen för kommandot `iostat` är:

```
iostat [alternativ] [argument]
```

## Vanliga alternativ
- `-c`: Visa endast CPU-statistik.
- `-d`: Visa endast I/O-statistik för blockenheter.
- `-x`: Visa utökad statistik för blockenheter.
- `-m`: Visa statistik i megabyte istället för block.
- `interval`: Ange tidsintervall mellan rapporter (i sekunder).
- `count`: Ange hur många rapporter som ska visas.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `iostat`:

1. Visa CPU- och I/O-statistik:
   ```bash
   iostat
   ```

2. Visa endast CPU-statistik:
   ```bash
   iostat -c
   ```

3. Visa I/O-statistik för blockenheter med utökad information:
   ```bash
   iostat -x
   ```

4. Visa statistik i megabyte var 5:e sekund, 3 gånger:
   ```bash
   iostat -m 5 3
   ```

5. Visa endast I/O-statistik för blockenheter:
   ```bash
   iostat -d
   ```

## Tips
- Använd `iostat` tillsammans med andra verktyg som `vmstat` och `top` för en mer komplett bild av systemets prestanda.
- Övervaka I/O-statistik regelbundet för att identifiera trender och potentiella problem innan de påverkar systemets prestanda.
- Experimentera med olika alternativ för att anpassa utdata efter dina behov och för att fokusera på specifika aspekter av systemets prestanda.