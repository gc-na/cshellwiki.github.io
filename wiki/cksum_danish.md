# [Linux] Bash cksum brug: Beregn checksum for filer

## Oversigt
`cksum`-kommandoen bruges til at beregne og vise checksum og byteantal for en eller flere filer. Det er nyttigt til at kontrollere integriteten af filer ved at sammenligne checksums.

## Brug
Den grundlæggende syntaks for `cksum`-kommandoen er:

```bash
cksum [muligheder] [argumenter]
```

## Almindelige muligheder
- `-a, --algorithm=ALGO`: Vælg en specifik algoritme til checksum-beregning.
- `--help`: Vis hjælp og afslut.
- `--version`: Vis versionsinformation.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `cksum`:

1. Beregn checksum for en enkelt fil:
   ```bash
   cksum fil.txt
   ```

2. Beregn checksum for flere filer:
   ```bash
   cksum fil1.txt fil2.txt fil3.txt
   ```

3. Gem output i en fil:
   ```bash
   cksum fil.txt > checksum.txt
   ```

4. Brug en specifik algoritme (hvis understøttet):
   ```bash
   cksum --algorithm=crc32 fil.txt
   ```

## Tips
- Brug `cksum` sammen med `diff` for at sammenligne checksums af to filer for at sikre, at de er identiske.
- Overvej at bruge `cksum` i scripts til automatisk at validere filintegritet efter overførsler eller ændringer.
- Husk at `cksum` kan returnere forskellige resultater afhængigt af filens indhold og format, så vær opmærksom på filtyperne, når du bruger kommandoen.