# [Linux] Bash mv användning: Flytta eller döpa om filer och kataloger

## Översikt
`mv`-kommandot används för att flytta eller döpa om filer och kataloger i Linux och andra Unix-liknande operativsystem. Det är ett grundläggande verktyg för filhantering.

## Användning
Den grundläggande syntaxen för `mv`-kommandot är:

```
mv [alternativ] [källa] [destination]
```

## Vanliga alternativ
- `-i`: Fråga innan en befintlig fil skrivs över.
- `-u`: Flytta endast om källan är nyare än destinationen eller om destinationen inte finns.
- `-v`: Visa detaljerad information om vad som flyttas.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mv`-kommandot:

1. **Flytta en fil till en annan katalog:**
   ```bash
   mv fil.txt /path/to/destination/
   ```

2. **Döpa om en fil:**
   ```bash
   mv gammalt_namn.txt nytt_namn.txt
   ```

3. **Flytta flera filer till en katalog:**
   ```bash
   mv fil1.txt fil2.txt /path/to/destination/
   ```

4. **Använda alternativet -i för att undvika att skriva över filer:**
   ```bash
   mv -i fil.txt /path/to/destination/
   ```

5. **Flytta en katalog:**
   ```bash
   mv /path/to/source_directory /path/to/destination_directory/
   ```

## Tips
- Använd `-v` för att se vad som händer när du flyttar filer, särskilt om du flyttar många filer på en gång.
- Kontrollera alltid att du har rätt sökvägar innan du kör kommandot, för att undvika oavsiktlig förlust av data.
- Överväg att använda `-i` för att förhindra oavsiktligt skrivande över filer.