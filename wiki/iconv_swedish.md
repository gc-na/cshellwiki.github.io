# [Linux] Bash iconv användning: Konvertera teckenkodningar

## Översikt
Kommandot `iconv` används för att konvertera textfiler mellan olika teckenkodningar. Det är ett kraftfullt verktyg för att hantera och omvandla textdata så att den kan läsas korrekt av olika program och system.

## Användning
Den grundläggande syntaxen för `iconv` är:

```bash
iconv [alternativ] [argument]
```

## Vanliga alternativ
- `-f, --from-code=KOD`: Anger den ursprungliga teckenkodningen.
- `-t, --to-code=KOD`: Anger den teckenkodning som texten ska konverteras till.
- `-o, --output=FIL`: Anger en utdatafil där den konverterade texten ska sparas.
- `-c`: Ignorerar ogiltiga tecken i indata.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `iconv`:

1. **Konvertera en fil från UTF-8 till ISO-8859-1:**

   ```bash
   iconv -f UTF-8 -t ISO-8859-1 input.txt -o output.txt
   ```

2. **Konvertera en fil och skriva ut resultatet till terminalen:**

   ```bash
   iconv -f UTF-8 -t UTF-16 input.txt
   ```

3. **Ignorera ogiltiga tecken under konvertering:**

   ```bash
   iconv -f UTF-8 -t ISO-8859-1 -c input.txt -o output.txt
   ```

4. **Konvertera flera filer i en loop:**

   ```bash
   for file in *.txt; do
       iconv -f UTF-8 -t ISO-8859-1 "$file" -o "converted_$file"
   done
   ```

## Tips
- Kontrollera alltid teckenkodningen på din indatafil innan du konverterar för att undvika dataförlust.
- Använd `iconv -l` för att lista alla tillgängliga teckenkodningar på ditt system.
- Testa konverteringen med en liten del av filen först för att säkerställa att resultatet blir som förväntat.