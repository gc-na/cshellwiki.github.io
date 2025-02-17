# [Linux] Bash grep användning: Sök efter mönster i text

## Översikt
Grep är ett kraftfullt verktyg i Bash som används för att söka efter specifika mönster i textfiler. Det kan användas för att filtrera ut rader som matchar ett givet mönster, vilket gör det ovärderligt för att analysera och hantera textdata.

## Användning
Den grundläggande syntaxen för grep är:

```
grep [alternativ] [mönster] [fil]
```

## Vanliga alternativ
- `-i`: Ignorera skillnader mellan stora och små bokstäver.
- `-v`: Visa rader som inte matchar mönstret.
- `-r`: Sök rekursivt i kataloger.
- `-n`: Visa radnummer för varje matchning.
- `-c`: Visa antalet matchningar istället för själva raderna.

## Vanliga exempel
Här är några praktiska exempel på hur grep kan användas:

1. Sök efter ett specifikt ord i en fil:
   ```bash
   grep "ord" fil.txt
   ```

2. Sök utan att ta hänsyn till stora och små bokstäver:
   ```bash
   grep -i "ord" fil.txt
   ```

3. Visa rader som inte innehåller ett visst ord:
   ```bash
   grep -v "ord" fil.txt
   ```

4. Sök rekursivt i alla filer i en katalog:
   ```bash
   grep -r "ord" /sökväg/till/katalog
   ```

5. Visa radnummer för varje matchning:
   ```bash
   grep -n "ord" fil.txt
   ```

## Tips
- Använd `grep -r` för att snabbt söka igenom hela projektkataloger.
- Kombinera grep med andra kommandon med hjälp av rör (`|`) för att skapa kraftfulla kommandokedjor.
- För att spara resultatet av en grep-sökning kan du omdirigera utdata till en fil med `>`:
  ```bash
  grep "ord" fil.txt > resultat.txt
  ```