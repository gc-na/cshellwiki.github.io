# [Linux] Bash od: Visning af filindhold i forskellige formater

## Oversigt
`od` (octal dump) er et kommandolinjeværktøj, der bruges til at vise indholdet af filer i forskellige formater, såsom oktal, hexadecimalt eller ASCII. Det er nyttigt til fejlfinding og analyse af binære filer.

## Brug
Den grundlæggende syntaks for `od`-kommandoen er:

```bash
od [muligheder] [argumenter]
```

## Almindelige muligheder
- `-A, --address-radix=RADIX`: Angiver adressens radix (f.eks. `d` for decimal, `o` for oktal, `x` for hex).
- `-t, --format=TYPE`: Angiver formatet for output (f.eks. `c` for karakterer, `d` for decimaler, `x` for hex).
- `-N, --read-bytes=N`: Angiver antallet af bytes, der skal læses fra filen.
- `-v, --output-duplicates`: Viser duplikerede linjer i output.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `od` kan bruges:

1. **Vis indholdet af en fil i oktal format:**
   ```bash
   od -c fil.txt
   ```

2. **Vis indholdet i hexadecimalt format:**
   ```bash
   od -x fil.bin
   ```

3. **Vis de første 16 bytes af en fil:**
   ```bash
   od -N 16 fil.bin
   ```

4. **Vis indholdet af en fil med adresser i decimal format:**
   ```bash
   od -A d -t x1 fil.bin
   ```

## Tips
- Brug `-v` for at sikre, at alle linjer vises, selv hvis de er duplikerede.
- Kombiner `od` med `less` for at navigere i store output:
  ```bash
  od fil.bin | less
  ```
- Eksperimenter med forskellige formater og muligheder for at få det ønskede output, især når du arbejder med forskellige filtyper.