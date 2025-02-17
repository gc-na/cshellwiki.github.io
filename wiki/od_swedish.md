# [Linux] Bash od användning: Visa filinnehåll i olika format

## Översikt
`od` (octal dump) är ett kommando i Unix-liknande operativsystem som används för att visa innehållet i filer i olika format, inklusive oktal, hexadecimalt och ASCII. Det är särskilt användbart för att inspektera binära filer eller för att se hur data är strukturerat.

## Användning
Den grundläggande syntaxen för `od` är:

```bash
od [alternativ] [argument]
```

## Vanliga alternativ
- `-A, --address-radix=RADIX`: Ställ in adressradix (t.ex. `d` för decimal, `o` för oktal, `x` för hex).
- `-t, --format=TYPE`: Ange formatet för utdata (t.ex. `c` för tecken, `d` för decimal, `x` för hex).
- `-N, --read-bytes=N`: Läs endast de första N byte av filen.
- `-v, --output-duplicates`: Visa alla dubbletter av data.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `od`:

1. Visa en fil i oktal format:
   ```bash
   od -c fil.txt
   ```

2. Visa en fil i hexadecimalt format:
   ```bash
   od -x fil.bin
   ```

3. Visa de första 16 byte av en fil i decimal:
   ```bash
   od -N 16 -t d1 fil.bin
   ```

4. Visa en fil med adressradix i hexadecimalt format:
   ```bash
   od -A x -t x1 fil.txt
   ```

## Tips
- Använd `-v` för att se alla dubbletter av data, vilket kan vara användbart när du arbetar med stora filer.
- Kombinera alternativ för att få en mer detaljerad utskrift, till exempel `od -A d -t x1 -N 32 fil.bin` för att visa både adress och hexadecimala värden.
- Tänk på att `od` är ett kraftfullt verktyg för att felsöka och analysera filer, så experimentera gärna med olika alternativ för att se vad som passar dina behov bäst.