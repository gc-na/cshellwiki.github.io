# [Linux] Bash find brug: Find filnavne

## Oversigt
`find`-kommandoen bruges til at søge efter filer og mapper i et filsystem baseret på specifikke kriterier. Den kan finde filer ved navn, type, størrelse, dato og meget mere.

## Brug
Den grundlæggende syntaks for `find`-kommandoen er:

```bash
find [stier] [betingelser] [handlinger]
```

## Almindelige muligheder
- `-name`: Søg efter filer med et bestemt navn.
- `-type`: Angiv filtypen (f.eks. `f` for filer, `d` for mapper).
- `-size`: Find filer baseret på størrelse (f.eks. `+100M` for større end 100 MB).
- `-mtime`: Find filer, der er ændret inden for et bestemt antal dage.
- `-exec`: Udfør en kommando på de fundne filer.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `find`:

1. **Find filer med et bestemt navn:**
   ```bash
   find /path/to/directory -name "filnavn.txt"
   ```

2. **Find alle mapper i en given sti:**
   ```bash
   find /path/to/directory -type d
   ```

3. **Find filer større end 100 MB:**
   ```bash
   find /path/to/directory -size +100M
   ```

4. **Find filer ændret inden for de sidste 7 dage:**
   ```bash
   find /path/to/directory -mtime -7
   ```

5. **Udfør en kommando på de fundne filer:**
   ```bash
   find /path/to/directory -name "*.log" -exec rm {} \;
   ```

## Tips
- Brug `-iname` i stedet for `-name` for at gøre søgningen case-insensitiv.
- Kombiner `find` med `grep` for at filtrere resultaterne yderligere.
- Vær forsigtig med `-exec`-muligheden, især når du sletter filer; dobbelttjek altid dine kriterier.