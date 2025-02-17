# [Linux] Bash blkid brug: Identificer blokenheder

## Oversigt
`blkid`-kommandoen bruges til at identificere blokenheder i Linux-systemer. Den viser information om enheder som harddiske, partitioner og USB-drev, herunder deres filsystemtype og UUID (Universally Unique Identifier).

## Brug
Den grundlæggende syntaks for `blkid`-kommandoen er:

```bash
blkid [options] [arguments]
```

## Almindelige muligheder
- `-o` : Angiv outputformat (f.eks. `value`, `full`).
- `-s` : Vælg specifikke attributter at vise (f.eks. `UUID`, `TYPE`).
- `-p` : Undgå at læse fra enhedens partitionstabel.
- `-c` : Angiv en cachefil til at gemme resultater.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `blkid`:

1. **Vis alle blokenheder:**
   ```bash
   blkid
   ```

2. **Vis specifik information om en enhed:**
   ```bash
   blkid /dev/sda1
   ```

3. **Vis kun UUID for en enhed:**
   ```bash
   blkid -s UUID -o value /dev/sda1
   ```

4. **Gem output til en fil:**
   ```bash
   blkid > blkid_output.txt
   ```

5. **Brug cache til hurtigere adgang:**
   ```bash
   blkid -c /etc/blkid.tab
   ```

## Tips
- Brug `blkid` med `sudo` for at få adgang til alle enheder, især hvis du får adgang til systempartitioner.
- Tjek regelmæssigt UUID'er for at sikre, at de ikke ændrer sig, hvilket kan påvirke systemets opstart.
- Overvej at bruge `blkid` i scripts til automatisk at identificere og håndtere blokenheder.