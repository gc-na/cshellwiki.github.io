# [Linux] Bash tail brug: Vis de sidste linjer i en fil

## Oversigt
`tail`-kommandoen bruges til at vise de sidste linjer af en fil. Det er nyttigt, når du ønsker at se de seneste opdateringer i logfiler eller store tekstfiler uden at åbne hele filen.

## Brug
Den grundlæggende syntaks for `tail`-kommandoen er:

```bash
tail [muligheder] [argumenter]
```

## Almindelige muligheder
- `-n [antal]`: Angiv antallet af linjer, der skal vises fra slutningen af filen. Standard er 10 linjer.
- `-f`: Følg filen, mens den opdateres. Dette er nyttigt til at overvåge logfiler i realtid.
- `-c [antal]`: Vis de sidste [antal] byte i stedet for linjer.

## Almindelige eksempler

1. **Vis de sidste 10 linjer af en fil:**
   ```bash
   tail filnavn.txt
   ```

2. **Vis de sidste 20 linjer af en fil:**
   ```bash
   tail -n 20 filnavn.txt
   ```

3. **Følg en logfil i realtid:**
   ```bash
   tail -f logfil.log
   ```

4. **Vis de sidste 50 byte af en fil:**
   ```bash
   tail -c 50 filnavn.txt
   ```

## Tips
- Brug `tail -f` sammen med `grep` for at filtrere specifikke linjer i realtid. For eksempel:
  ```bash
  tail -f logfil.log | grep "fejl"
  ```
- Kombiner `tail` med `head` for at se et specifikt interval af linjer fra slutningen af en fil:
  ```bash
  tail -n 100 filnavn.txt | head -n 10
  ```
- Hvis du arbejder med store logfiler, kan `tail` være en hurtigere måde at få indsigt i filens indhold uden at åbne hele filen.