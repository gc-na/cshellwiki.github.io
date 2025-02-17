# [Linux] Bash ls Användning: Lista filer och kataloger

## Översikt
Kommandot `ls` används för att lista filer och kataloger i ett angivet katalog. Det är ett av de mest grundläggande och använda kommandona i Bash, vilket gör det enkelt att se innehållet i en katalog.

## Användning
Den grundläggande syntaxen för `ls` är:

```
ls [alternativ] [argument]
```

## Vanliga alternativ
- `-l`: Visar detaljerad information om filer och kataloger, inklusive behörigheter, ägare, storlek och datum för senaste ändring.
- `-a`: Visar alla filer, inklusive dolda filer som börjar med en punkt (.)
- `-h`: Visar storlekar i ett mänskligt läsbart format (t.ex. KB, MB).
- `-R`: Visar innehållet i kataloger rekursivt.
- `-t`: Sorterar filer efter tid, med de senaste ändrade filerna först.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `ls`:

1. Lista filer i den aktuella katalogen:
   ```bash
   ls
   ```

2. Lista alla filer, inklusive dolda:
   ```bash
   ls -a
   ```

3. Lista filer med detaljerad information:
   ```bash
   ls -l
   ```

4. Lista filer med detaljerad information och mänskligt läsbara storlekar:
   ```bash
   ls -lh
   ```

5. Lista filer sorterade efter senaste ändring:
   ```bash
   ls -lt
   ```

6. Lista filer rekursivt i alla underkataloger:
   ```bash
   ls -R
   ```

## Tips
- Använd `ls -lh` för att snabbt få en översikt över filstorlekar i ett lättläst format.
- Kombinera alternativ för att få mer specifik information, till exempel `ls -la` för att se alla filer med detaljerad information.
- Om du ofta arbetar i en specifik katalog, överväg att använda alias för att förenkla dina kommandon.