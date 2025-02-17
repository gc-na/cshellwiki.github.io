# [Linux] Bash rev: vänd textsträngar

## Översikt
`rev` är ett Bash-kommando som används för att vända varje rad av text i en fil eller från standardinmatning. Det är ett enkelt men kraftfullt verktyg för att manipulera textdata.

## Användning
Den grundläggande syntaxen för kommandot är:

```
rev [alternativ] [argument]
```

## Vanliga alternativ
- `-o, --output=FILNAMN` : Skriv ut resultatet till den angivna filen istället för standardutmatningen.
- `-h, --help` : Visa hjälpmeddelande och avsluta.
- `-V, --version` : Visa versionsinformation och avsluta.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `rev`:

1. **Vända text från standardinmatning:**
   ```bash
   echo "Hej världen" | rev
   ```
   Utdata:
   ```
   nedlrew jHe
   ```

2. **Vända innehållet i en fil:**
   Anta att du har en fil som heter `text.txt` med följande innehåll:
   ```
   Första raden
   Andra raden
   ```
   Du kan vända varje rad i filen så här:
   ```bash
   rev text.txt
   ```
   Utdata:
   ```
   nadar atsroF
   nadar ardnA
   ```

3. **Skriva ut resultatet till en ny fil:**
   ```bash
   rev text.txt -o omvänd.txt
   ```
   Detta kommando vänder innehållet i `text.txt` och sparar det i `omvänd.txt`.

## Tips
- Använd `rev` tillsammans med andra kommandon i en pipeline för att effektivt bearbeta textdata.
- Kontrollera alltid resultatet av `rev` när du arbetar med viktiga filer för att säkerställa att data har manipulerats som avsett.
- `rev` fungerar bäst med textfiler, så se till att filerna är i rätt format för att undvika oväntade resultat.