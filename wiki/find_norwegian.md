# [Linux] Bash find bruk: Finn filnavn

## Oversikt
`find`-kommandoen brukes til å søke etter filer og kataloger i et filsystem basert på spesifikke kriterier. Den kan søke i en angitt katalog og dens underkataloger, og den gir mulighet for å filtrere resultater basert på navn, type, størrelse, og mer.

## Bruk
Grunnleggende syntaks for `find`-kommandoen er som følger:

```bash
find [alternativer] [argumenter]
```

## Vanlige alternativer
- `-name`: Søker etter filer med et spesifikt navn.
- `-type`: Filtrerer resultater basert på filtype (f.eks. `f` for filer, `d` for kataloger).
- `-size`: Søker etter filer basert på størrelse.
- `-mtime`: Filtrerer filer basert på når de sist ble endret.
- `-exec`: Utfører en kommando på hver fil som blir funnet.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan `find` kan brukes:

### 1. Finne filer med spesifikt navn
```bash
find /path/to/directory -name "filnavn.txt"
```

### 2. Finne alle kataloger
```bash
find /path/to/directory -type d
```

### 3. Finne filer større enn 1 GB
```bash
find /path/to/directory -size +1G
```

### 4. Finne filer endret de siste 7 dagene
```bash
find /path/to/directory -mtime -7
```

### 5. Slette filer med spesifikt navn
```bash
find /path/to/directory -name "filnavn.txt" -exec rm {} \;
```

## Tips
- Bruk `-iname` i stedet for `-name` for å gjøre søket case-insensitivt.
- Kombiner flere alternativer for mer presise søk, for eksempel `find /path -type f -name "*.log" -mtime -30` for å finne loggfiler som er endret de siste 30 dagene.
- Vær forsiktig med `-exec`-alternativet, spesielt når du bruker det med kommandoer som `rm`, da dette kan føre til tap av data hvis det ikke brukes riktig.