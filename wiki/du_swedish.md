# [Linux] Bash du: Visa diskanvändning

## Översikt
`du` (disk usage) är ett kommandoradsverktyg som används för att visa hur mycket diskutrymme som används av filer och kataloger. Det ger en sammanställning av storleken på filer och mappar i ett angivet sökväg.

## Användning
Den grundläggande syntaxen för `du` är:

```bash
du [alternativ] [argument]
```

## Vanliga alternativ
- `-h`: Visar storlekar i ett läsbart format (t.ex. KB, MB, GB).
- `-s`: Visar endast den totala storleken för varje angiven katalog.
- `-a`: Visar storleken för alla filer, inte bara kataloger.
- `-c`: Ger en sammanställning av storlekarna i slutet av utdata.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `du`:

1. Visa diskanvändning för den aktuella katalogen:
   ```bash
   du
   ```

2. Visa diskanvändning i ett läsbart format:
   ```bash
   du -h
   ```

3. Visa den totala storleken för en specifik katalog:
   ```bash
   du -sh /path/to/directory
   ```

4. Visa storleken på alla filer och kataloger i den aktuella katalogen:
   ```bash
   du -a
   ```

5. Visa diskanvändning för en katalog och inkludera en sammanställning:
   ```bash
   du -ch /path/to/directory
   ```

## Tips
- Använd `du -h` för att enkelt läsa storlekar, särskilt när du arbetar med stora kataloger.
- Kombinera `du` med `sort` för att sortera utdata efter storlek:
  ```bash
  du -h | sort -h
  ```
- För att snabbt identifiera stora filer och kataloger, kan du använda `du -sh *` i en katalog för att få en översikt över storlekarna.