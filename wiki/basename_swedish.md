# [Linux] Bash basename användning: Extrahera filnamn från sökvägar

## Översikt
Kommandot `basename` används för att extrahera filnamnet från en given sökväg. Det tar bort alla ledande kataloger och lämnar endast namnet på filen eller mappen.

## Användning
Den grundläggande syntaxen för `basename` är:

```bash
basename [alternativ] [argument]
```

## Vanliga alternativ
- `-a`: Behandla flera argument och returnera varje filnamn på en ny rad.
- `-s`: Ta bort en specifik suffix från filnamnet.
- `--help`: Visa hjälpmeddelande för kommandot.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `basename`:

1. Extrahera filnamnet från en sökväg:
   ```bash
   basename /home/user/documents/file.txt
   ```
   Utdata:
   ```
   file.txt
   ```

2. Ta bort en specifik suffix:
   ```bash
   basename /home/user/documents/file.txt .txt
   ```
   Utdata:
   ```
   file
   ```

3. Hantera flera sökvägar:
   ```bash
   basename -a /home/user/documents/file1.txt /home/user/documents/file2.txt
   ```
   Utdata:
   ```
   file1.txt
   file2.txt
   ```

## Tips
- Använd `basename` i skript för att enkelt hantera filnamn utan att behöva bearbeta hela sökvägen.
- Kombinera `basename` med andra kommandon, som `find`, för att få en lista över filnamn i en katalog.
- Tänk på att om du använder suffixalternativet, måste du ange det exakta suffixet för att det ska tas bort korrekt.