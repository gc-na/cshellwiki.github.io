# [Linux] Bash wc användning: Räkna rader, ord och tecken

## Översikt
`wc` (word count) är ett Bash-kommando som används för att räkna antalet rader, ord och tecken i en fil eller i standardinmatning. Det är ett enkelt men kraftfullt verktyg för att analysera textfiler.

## Användning
Den grundläggande syntaxen för `wc` är:

```bash
wc [alternativ] [argument]
```

## Vanliga alternativ
- `-l`: Räknar antalet rader.
- `-w`: Räknar antalet ord.
- `-c`: Räknar antalet tecken.
- `-m`: Räknar antalet tecken (inklusive flerbyte-tecken).
- `-L`: Visar längden på den längsta raden.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `wc`:

1. Räkna antalet rader i en fil:
   ```bash
   wc -l filnamn.txt
   ```

2. Räkna antalet ord i en fil:
   ```bash
   wc -w filnamn.txt
   ```

3. Räkna antalet tecken i en fil:
   ```bash
   wc -c filnamn.txt
   ```

4. Räkna rader, ord och tecken samtidigt:
   ```bash
   wc filnamn.txt
   ```

5. Räkna antalet tecken i en textsträng som matas in via standardinmatning:
   ```bash
   echo "Hej världen" | wc -c
   ```

## Tips
- Använd `wc` tillsammans med andra kommandon genom att använda rör (`|`) för att analysera utdata från andra verktyg.
- För att få en snabb översikt över en fil, använd `wc` utan några alternativ för att se rader, ord och tecken i en enda rad.
- Tänk på att `wc` kan hantera flera filer samtidigt. Om du anger flera filnamn kommer `wc` att ge en sammanfattning för varje fil samt en totalräkning.