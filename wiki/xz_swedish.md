# [Linux] Bash xz Användning: Komprimera och dekomprimera filer

## Översikt
Kommandot `xz` används för att komprimera och dekomprimera filer med hjälp av LZMA-algoritmen. Det är känt för att ge hög komprimeringsgrad, vilket gör det populärt för att minska filstorlekar.

## Användning
Den grundläggande syntaxen för `xz` är:

```bash
xz [alternativ] [argument]
```

## Vanliga alternativ
- `-d`, `--decompress`: Dekomprimera en fil.
- `-k`, `--keep`: Behåll den ursprungliga filen efter komprimering.
- `-f`, `--force`: Tvinga komprimering eller dekomprimering, även om det finns en fil med samma namn.
- `-z`, `--compress`: Komprimera en fil (standardbeteende).
- `-9`: Använd maximal komprimering.

## Vanliga exempel
Komprimera en fil:

```bash
xz fil.txt
```

Dekomprimera en fil:

```bash
xz -d fil.txt.xz
```

Komprimera en fil och behåll den ursprungliga:

```bash
xz -k fil.txt
```

Tvinga komprimering av en fil, även om en fil med samma namn finns:

```bash
xz -f fil.txt
```

Komprimera med maximal komprimering:

```bash
xz -9 fil.txt
```

## Tips
- Använd `-k` om du vill behålla den ursprungliga filen för säkerhets skull.
- Tänk på att `xz` kan ta längre tid att komprimera jämfört med andra verktyg, men det ger ofta bättre komprimeringsresultat.
- För att se komprimeringsstatus och filinformation, använd `xz -l fil.txt.xz`.