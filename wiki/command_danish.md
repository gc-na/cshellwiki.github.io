# [Linux] Bash command brug: [find filnavne]

## Oversigt
`find`-kommandoen bruges til at søge efter filer og mapper i et filsystem baseret på specifikke kriterier. Den kan finde filer ved hjælp af forskellige parametre som navn, type, størrelse og ændringsdato.

## Brug
Den grundlæggende syntaks for `find`-kommandoen er:

```bash
find [stien] [betingelser] [handlinger]
```

## Almindelige muligheder
- `-name`: Søg efter filer med et bestemt navn.
- `-type`: Angiv filtype (f.eks. `f` for almindelige filer, `d` for mapper).
- `-size`: Søg efter filer baseret på størrelse (f.eks. `+100k` for filer større end 100 KB).
- `-mtime`: Find filer ændret inden for et bestemt antal dage.
- `-exec`: Udfør en kommando på de fundne filer.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `find`-kommandoen kan bruges:

1. **Find filer med et bestemt navn:**
   ```bash
   find /path/to/search -name "filnavn.txt"
   ```

2. **Find alle mapper i en given sti:**
   ```bash
   find /path/to/search -type d
   ```

3. **Find filer større end 1 MB:**
   ```bash
   find /path/to/search -size +1M
   ```

4. **Find filer ændret i løbet af de sidste 7 dage:**
   ```bash
   find /path/to/search -mtime -7
   ```

5. **Slet alle `.tmp` filer i en mappe:**
   ```bash
   find /path/to/search -name "*.tmp" -exec rm {} \;
   ```

## Tips
- Brug `-iname` i stedet for `-name` for at gøre søgningen case-insensitiv.
- Vær forsigtig med `-exec`-muligheden, da den kan udføre potentielt destruktive handlinger. Test først med `-print` for at se, hvilke filer der vil blive påvirket.
- Kombiner flere betingelser ved hjælp af `-and` og `-or` for mere komplekse søgninger.