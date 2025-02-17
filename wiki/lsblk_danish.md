# [Linux] Bash lsblk Brug: Visning af blokenheder

## Oversigt
`lsblk` er en Bash-kommando, der bruges til at vise information om blokenheder i systemet. Den viser en liste over alle tilsluttede blokenheder, såsom harddiske, SSD'er og USB-drev, samt deres partitioner og monteringspunkter.

## Brug
Den grundlæggende syntaks for `lsblk`-kommandoen er:

```bash
lsblk [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a`, `--all`: Vis alle enheder, inklusive tomme.
- `-f`, `--fs`: Vis filsysteminformation.
- `-l`, `--list`: Vis output i listeformat.
- `-o`, `--output`: Angiv specifikke kolonner, der skal vises.
- `-p`, `--paths`: Vis fulde enhedsnavne.

## Almindelige eksempler

1. **Vis alle blokenheder**:
   ```bash
   lsblk
   ```

2. **Vis blokenheder med filsysteminformation**:
   ```bash
   lsblk -f
   ```

3. **Vis blokenheder i listeformat**:
   ```bash
   lsblk -l
   ```

4. **Vis specifikke kolonner**:
   ```bash
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

5. **Vis alle enheder, inklusive tomme**:
   ```bash
   lsblk -a
   ```

## Tips
- Brug `lsblk -f` for hurtigt at se, hvilke filsystemer der er på hver enhed.
- Kombiner `lsblk` med `grep` for at filtrere output, hvis du leder efter en specifik enhed.
- For en mere detaljeret visning, kan du overveje at bruge `lsblk -o +UUID` for at inkludere UUID'er i outputtet.