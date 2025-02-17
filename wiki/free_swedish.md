# [Linux] Bash free användning: Visa minnesanvändning

## Översikt
Kommandot `free` används för att visa information om systemets minnesanvändning. Det ger en översikt över det totala, använda och lediga minnet, samt buffertar och cacheminne.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
free [alternativ]
```

## Vanliga alternativ
- `-h`: Visar minnesinformation i ett mer läsbart format (t.ex. MB eller GB).
- `-m`: Visar minnesinformation i megabyte.
- `-g`: Visar minnesinformation i gigabyte.
- `-s [sekunder]`: Uppdaterar visningen med det angivna intervallet i sekunder.
- `-t`: Inkluderar en totalrad för minnesanvändning.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `free`:

1. Visa minnesanvändning i standardformat:
   ```bash
   free
   ```

2. Visa minnesanvändning i ett läsbart format:
   ```bash
   free -h
   ```

3. Visa minnesanvändning i megabyte:
   ```bash
   free -m
   ```

4. Visa minnesanvändning i gigabyte:
   ```bash
   free -g
   ```

5. Uppdatera minnesinformation var 5:e sekund:
   ```bash
   free -s 5
   ```

6. Visa total minnesanvändning:
   ```bash
   free -t
   ```

## Tips
- Använd `free -h` för att snabbt få en översikt över minnesanvändningen i ett lättförståeligt format.
- Kombinera `free` med andra kommandon som `watch` för att kontinuerligt övervaka minnesanvändningen:
  ```bash
  watch free -h
  ```
- Tänk på att `free` visar minnesanvändning i realtid, så det kan vara bra att köra det flera gånger för att se förändringar över tid.