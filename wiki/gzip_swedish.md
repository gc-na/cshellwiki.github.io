# [Linux] Bash gzip användning: Komprimera filer

## Översikt
`gzip` är ett kommandoradsverktyg som används för att komprimera filer i Unix-liknande operativsystem. Det minskar filstorleken genom att använda Lempel-Ziv algoritmen, vilket gör det enklare att lagra och överföra filer.

## Användning
Den grundläggande syntaxen för `gzip` är:

```bash
gzip [alternativ] [argument]
```

## Vanliga alternativ
- `-d` eller `--decompress`: Dekomprimerar en gzip-komprimerad fil.
- `-k` eller `--keep`: Bevarar den ursprungliga filen efter komprimering.
- `-v` eller `--verbose`: Visar detaljerad information om komprimeringsprocessen.
- `-r` eller `--recursive`: Komprimerar filer i alla underkataloger.
- `-f` eller `--force`: Tvingar komprimering även om det finns problem med filerna.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `gzip`:

1. **Komprimera en fil:**
   ```bash
   gzip fil.txt
   ```
   Detta skapar en komprimerad fil som heter `fil.txt.gz`.

2. **Dekomprimera en fil:**
   ```bash
   gzip -d fil.txt.gz
   ```
   Detta återställer den komprimerade filen till sitt ursprungliga tillstånd.

3. **Bevara den ursprungliga filen vid komprimering:**
   ```bash
   gzip -k fil.txt
   ```
   Denna kommando komprimerar `fil.txt` men behåller även den ursprungliga filen.

4. **Komprimera alla `.txt`-filer i en katalog:**
   ```bash
   gzip *.txt
   ```
   Detta komprimerar alla textfiler i den aktuella katalogen.

5. **Komprimera filer rekursivt i en katalog:**
   ```bash
   gzip -r /sökväg/till/katalog
   ```
   Detta komprimerar alla filer i den angivna katalogen och dess underkataloger.

## Tips
- Använd `gzip -v` för att få en översikt över hur mycket utrymme du sparar efter komprimering.
- Tänk på att komprimerade filer inte kan öppnas direkt; du måste dekomprimera dem först.
- För att komprimera stora filer eller kataloger, överväg att använda `tar` tillsammans med `gzip` för att skapa en arkivfil.