# [Linux] Bash sha256sum användning: Beräkna SHA-256 hashvärden

## Översikt
Kommandot `sha256sum` används för att beräkna och verifiera SHA-256 hashvärden för filer. Det är ett viktigt verktyg för att säkerställa dataintegritet och kan användas för att kontrollera om en fil har förändrats.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
sha256sum [alternativ] [argument]
```

## Vanliga alternativ
- `-b`, `--binary`: Behandla filen som en binär fil.
- `-c`, `--check`: Kontrollera hashvärdena mot en given lista.
- `--tag`: Skriv ut hashvärdena i en taggad format.

## Vanliga exempel

1. Beräkna SHA-256 hashvärdet för en fil:
   ```bash
   sha256sum fil.txt
   ```

2. Spara hashvärdet till en fil:
   ```bash
   sha256sum fil.txt > hash.txt
   ```

3. Kontrollera hashvärdena mot en lista:
   Först, skapa en fil med hashvärden:
   ```bash
   sha256sum fil.txt > hash.txt
   ```
   Sedan, kontrollera:
   ```bash
   sha256sum -c hash.txt
   ```

4. Beräkna hashvärdet för flera filer:
   ```bash
   sha256sum fil1.txt fil2.txt
   ```

## Tips
- Använd `-b` alternativet om du arbetar med binära filer för att säkerställa korrekt hashberäkning.
- Kontrollera alltid hashvärden efter nedladdning av filer för att säkerställa att de inte har blivit korrupta.
- För att enkelt jämföra hashvärden, kan du använda `-c` alternativet med en lista över förväntade hashvärden.