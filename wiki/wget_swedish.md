# [Linux] Bash wget användning: Ladda ner filer från webben

## Översikt
`wget` är ett kraftfullt kommandoradsverktyg som används för att ladda ner filer från webben. Det stöder olika protokoll som HTTP, HTTPS och FTP, vilket gör det till ett mångsidigt verktyg för att hämta filer, hela webbplatser eller till och med för att återuppta avbrutna nedladdningar.

## Användning
Den grundläggande syntaxen för `wget` är:

```
wget [alternativ] [argument]
```

## Vanliga alternativ
- `-O [filnamn]`: Spara den nedladdade filen med ett specifikt namn.
- `-c`: Fortsätt en avbruten nedladdning.
- `-r`: Ladda ner en hel webbplats rekursivt.
- `-p`: Ladda ner alla resurser som behövs för att visa en webbsida (bilder, CSS, etc.).
- `--limit-rate=[hastighet]`: Begränsa nedladdningshastigheten.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `wget`:

1. Ladda ner en fil:
   ```bash
   wget https://example.com/fil.zip
   ```

2. Spara filen med ett specifikt namn:
   ```bash
   wget -O minfil.zip https://example.com/fil.zip
   ```

3. Fortsätt en avbruten nedladdning:
   ```bash
   wget -c https://example.com/fil.zip
   ```

4. Ladda ner en hel webbplats:
   ```bash
   wget -r https://example.com
   ```

5. Ladda ner en webbsida och alla dess resurser:
   ```bash
   wget -p https://example.com/sida.html
   ```

## Tips
- Använd `-q` för att köra `wget` i tyst läge, vilket minskar mängden utskrift.
- Kombinera `-r` med `--no-parent` för att undvika att ladda ner filer från överordnade kataloger.
- Kontrollera alltid nedladdningslänkar för att säkerställa att de är giltiga och säkra innan du laddar ner.