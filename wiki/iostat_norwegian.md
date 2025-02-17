# [Linux] Bash iostat Bruk: Overvåk systemytelse

## Oversikt
`iostat` er et verktøy som brukes til å overvåke systemytelse, spesielt disk I/O (input/output) og CPU-bruk. Det gir informasjon om hvor mye tid systemet bruker på å lese og skrive til disker, samt CPU-bruken, noe som kan hjelpe med feilsøking og ytelsesoptimalisering.

## Bruk
Grunnleggende syntaks for `iostat`-kommandoen er:

```bash
iostat [alternativer] [argumenter]
```

## Vanlige alternativer
- `-c`: Viser CPU-statistikk.
- `-d`: Viser diskstatistikk.
- `-x`: Viser utvidet diskstatistikk.
- `-k`: Viser statistikk i kilobyte per sekund.
- `-m`: Viser statistikk i megabyte per sekund.
- `-t`: Viser tidsstempel for hver rapport.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `iostat`:

1. **Vis CPU-statistikk:**
   ```bash
   iostat -c
   ```

2. **Vis diskstatistikk:**
   ```bash
   iostat -d
   ```

3. **Vis både CPU- og diskstatistikk:**
   ```bash
   iostat -c -d
   ```

4. **Vis utvidet diskstatistikk i megabyte per sekund:**
   ```bash
   iostat -x -m
   ```

5. **Vis statistikk med tidsintervall på 5 sekunder:**
   ```bash
   iostat 5
   ```

## Tips
- Bruk `iostat` sammen med andre verktøy som `top` eller `vmstat` for en mer omfattende analyse av systemytelsen.
- Overvåk systemet over tid for å identifisere mønstre i ytelsen og finne flaskehalser.
- Tenk på å bruke `-t` alternativet for å få tidsstempler, noe som kan være nyttig for logging og analyse.