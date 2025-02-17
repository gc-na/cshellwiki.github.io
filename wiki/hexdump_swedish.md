# [Linux] Bash hexdump användning: Visa binära data i hexadecimalt format

## Översikt
Hexdump-kommandot används för att visa innehållet i en fil i ett hexadecimalt format. Det är ett användbart verktyg för att inspektera binära filer och förstå deras struktur.

## Användning
Den grundläggande syntaxen för hexdump-kommandot är:

```bash
hexdump [alternativ] [argument]
```

## Vanliga alternativ
- `-C`: Visar hexdump i en mer läsbar format, med både hexadecimala värden och ASCII-representation.
- `-n N`: Anger att endast de första N byte ska visas.
- `-s N`: Hoppar över de första N byte i filen innan dumpningen börjar.
- `-v`: Visar alla data, inklusive upprepade byte.

## Vanliga exempel
Här är några praktiska exempel på hur man använder hexdump:

1. Visa hela innehållet i en fil i hexadecimalt format:
   ```bash
   hexdump fil.txt
   ```

2. Visa de första 16 byte av en fil:
   ```bash
   hexdump -n 16 fil.txt
   ```

3. Visa en fil med både hexadecimala värden och ASCII-representation:
   ```bash
   hexdump -C fil.txt
   ```

4. Hoppa över de första 10 byte och visa resten:
   ```bash
   hexdump -s 10 fil.txt
   ```

5. Visa en fil och inkludera alla data, även upprepningar:
   ```bash
   hexdump -v fil.txt
   ```

## Tips
- Använd `-C` för att göra utdata mer läsbara, särskilt när du arbetar med textfiler.
- Tänk på att hexdump kan visa stora filer, så använd `-n` och `-s` för att begränsa mängden data som visas.
- Kombinera hexdump med andra kommandon, som `less`, för att enkelt bläddra igenom stora mängder data:
  ```bash
  hexdump fil.txt | less
  ```