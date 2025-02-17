# [Linux] Bash comm användning: Jämför två sorterade filer

## Översikt
`comm`-kommandot används för att jämföra två sorterade filer rad för rad. Det visar skillnader och likheter mellan dem, vilket gör det till ett användbart verktyg för att analysera innehåll i textfiler.

## Användning
Den grundläggande syntaxen för `comm`-kommandot är:

```bash
comm [alternativ] [fil1] [fil2]
```

## Vanliga alternativ
- `-1`: Undertryck raden som endast finns i den första filen.
- `-2`: Undertryck raden som endast finns i den andra filen.
- `-3`: Undertryck raden som finns i båda filerna.
- `-i`: Ignorera skillnader i versaler och gemener.
- `-d`: Visa endast dubbletter.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `comm`:

1. Jämföra två filer och visa alla rader:
   ```bash
   comm fil1.txt fil2.txt
   ```

2. Visa endast rader som finns i den första filen:
   ```bash
   comm -13 fil1.txt fil2.txt
   ```

3. Visa endast rader som finns i den andra filen:
   ```bash
   comm -12 fil1.txt fil2.txt
   ```

4. Ignorera skillnader i versaler och gemener:
   ```bash
   comm -i fil1.txt fil2.txt
   ```

5. Visa endast dubbletter mellan två filer:
   ```bash
   comm -d fil1.txt fil2.txt
   ```

## Tips
- Se till att filerna är sorterade innan du använder `comm`, annars kan resultaten bli felaktiga.
- Använd `sort`-kommandot för att sortera filerna om de inte redan är det:
  ```bash
  sort fil1.txt -o fil1.txt
  sort fil2.txt -o fil2.txt
  ```
- Kombinera `comm` med andra kommandon i en pipeline för mer avancerad analys av filinnehåll.