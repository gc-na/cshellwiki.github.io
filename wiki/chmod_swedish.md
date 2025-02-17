# [Linux] Bash chmod användning: Ändra filbehörigheter

## Översikt
`chmod` (change mode) är ett kommando i Unix-liknande operativsystem som används för att ändra behörigheterna för filer och kataloger. Det gör det möjligt för användare att styra vem som kan läsa, skriva eller köra en fil.

## Användning
Den grundläggande syntaxen för `chmod` är:

```bash
chmod [alternativ] [argument]
```

## Vanliga alternativ
- `-R`: Ändra behörigheter rekursivt för alla filer och underkataloger.
- `u`: Refererar till ägaren av filen (user).
- `g`: Refererar till gruppen som äger filen (group).
- `o`: Refererar till andra användare (others).
- `r`: Ger läsbehörighet (read).
- `w`: Ger skrivbehörighet (write).
- `x`: Ger körbehörighet (execute).
- `+`: Lägger till en behörighet.
- `-`: Tar bort en behörighet.
- `=`: Sätter en specifik behörighet.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `chmod`:

1. Ge ägaren läs- och skrivbehörighet:
   ```bash
   chmod u+rw fil.txt
   ```

2. Ta bort körbehörighet för andra användare:
   ```bash
   chmod o-x fil.txt
   ```

3. Ge alla användare läsbehörighet:
   ```bash
   chmod a+r fil.txt
   ```

4. Ändra behörigheter rekursivt för en katalog:
   ```bash
   chmod -R 755 katalog/
   ```

5. Sätta specifika behörigheter för en fil:
   ```bash
   chmod 644 fil.txt
   ```

## Tips
- Använd `ls -l` för att kontrollera aktuella behörigheter innan du gör ändringar.
- Var försiktig med att ge för mycket behörighet, särskilt skriv- och körbehörighet, för att undvika säkerhetsrisker.
- Använd `chmod` med `sudo` om du behöver ändra behörigheter för filer som ägs av andra användare eller systemfiler.