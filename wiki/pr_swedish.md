# [Linux] Bash pr användning: Formatera textfiler för utskrift

## Översikt
`pr` är ett Bash-kommando som används för att formatera textfiler för utskrift. Det delar upp texten i kolumner och lägger till sidhuvuden och sidnummer, vilket gör det enklare att läsa och skriva ut långa dokument.

## Användning
Den grundläggande syntaxen för `pr` är:

```
pr [alternativ] [argument]
```

## Vanliga alternativ
- `-h` : Anger en anpassad rubrik för varje sida.
- `-l` : Anger antalet rader per sida.
- `-n` : Visar sidnummer i marginalen.
- `-t` : Tar bort tomma rader mellan sidor.
- `-s` : Anger ett specifikt tecken som ska användas som avgränsare mellan kolumner.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `pr`:

1. Formatera en textfil med standardinställningar:
   ```bash
   pr minfil.txt
   ```

2. Ange en rubrik för utskriften:
   ```bash
   pr -h "Min Rubrik" minfil.txt
   ```

3. Ställ in antalet rader per sida till 50:
   ```bash
   pr -l 50 minfil.txt
   ```

4. Visa sidnummer i marginalen:
   ```bash
   pr -n minfil.txt
   ```

5. Dela upp flera filer i kolumner:
   ```bash
   pr fil1.txt fil2.txt
   ```

## Tips
- Använd `-t` om du vill ha en mer kompakt utskrift utan extra tomma rader.
- Experimentera med olika kolumninställningar för att se vad som passar bäst för din text.
- Kombinera `pr` med andra kommandon som `less` för att bläddra i långa dokument:
  ```bash
  pr minfil.txt | less
  ```