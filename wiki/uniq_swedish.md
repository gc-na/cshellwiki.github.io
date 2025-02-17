# [Linux] Bash uniq användning: Ta bort dubbletter från en fil

## Översikt
`uniq` är ett Bash-kommando som används för att ta bort dubbletter från en sorterad lista. Det fungerar genom att jämföra på varandra följande rader och endast behålla den första av varje uppsättning av dubbletter.

## Användning
Den grundläggande syntaxen för `uniq` är:

```bash
uniq [alternativ] [argument]
```

## Vanliga alternativ
- `-c`: Räkna antalet förekomster av varje rad.
- `-d`: Visa endast rader som är dubbletter.
- `-u`: Visa endast rader som är unika.
- `-i`: Ignorera skillnader mellan stora och små bokstäver.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `uniq`:

1. Ta bort dubbletter från en fil:
   ```bash
   uniq fil.txt
   ```

2. Räkna antalet förekomster av varje rad:
   ```bash
   uniq -c fil.txt
   ```

3. Visa endast dubbletter:
   ```bash
   uniq -d fil.txt
   ```

4. Ignorera stora och små bokstäver när man tar bort dubbletter:
   ```bash
   uniq -i fil.txt
   ```

5. Kombinera `uniq` med `sort` för att ta bort dubbletter från en osorterad lista:
   ```bash
   sort fil.txt | uniq
   ```

## Tips
- Se till att din fil är sorterad innan du använder `uniq`, annars kanske inte dubbletterna tas bort korrekt.
- Använd `sort` i kombination med `uniq` för att säkerställa att alla dubbletter tas bort, oavsett deras position i filen.
- Experimentera med olika alternativ för att få den information du behöver, till exempel att räkna dubbletter eller visa unika rader.