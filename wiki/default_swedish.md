# [Linux] Bash standardkommandot `ls`: listar filer och kataloger

## Översikt
Kommandot `ls` används för att lista filer och kataloger i en specifik katalog. Det är ett av de mest grundläggande och använda kommandona i Bash, vilket gör det enkelt att se innehållet i en katalog.

## Användning
Den grundläggande syntaxen för kommandot `ls` är:

```bash
ls [alternativ] [argument]
```

## Vanliga alternativ
- `-l`: Visar detaljerad information om varje fil och katalog, inklusive rättigheter, ägare, storlek och datum för senaste ändring.
- `-a`: Visar alla filer, inklusive dolda filer som börjar med en punkt (.)
- `-h`: Visar storlekar i ett läsbart format (t.ex. KB, MB) när det används med `-l`.
- `-R`: Visar innehållet i underkataloger rekursivt.
- `-t`: Sorterar filer efter tid, så att de senaste ändringarna visas först.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `ls`:

1. Lista alla filer och kataloger i den aktuella katalogen:
   ```bash
   ls
   ```

2. Lista alla filer, inklusive dolda filer:
   ```bash
   ls -a
   ```

3. Lista filer med detaljerad information:
   ```bash
   ls -l
   ```

4. Lista filer med detaljerad information och läsbara storlekar:
   ```bash
   ls -lh
   ```

5. Lista filer i en katalog rekursivt:
   ```bash
   ls -R
   ```

6. Lista filer sorterade efter senaste ändring:
   ```bash
   ls -lt
   ```

## Tips
- Använd `ls --color` för att få färgkodade utdata, vilket gör det lättare att skilja mellan filer och kataloger.
- Kombinera alternativ för att få mer specifik information, till exempel `ls -la` för att se alla filer med detaljerad information.
- Om du ofta behöver lista filer i en specifik katalog, kan du ange sökvägen direkt, t.ex. `ls /path/to/directory`.