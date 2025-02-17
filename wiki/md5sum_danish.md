# [Linux] Bash md5sum brug: Beregn MD5-hash for filer

## Oversigt
`md5sum` er et Bash-kommando, der bruges til at beregne og kontrollere MD5-hash-værdier for filer. Det er nyttigt til at sikre integriteten af data ved at sammenligne hash-værdier.

## Brug
Den grundlæggende syntaks for `md5sum`-kommandoen er:

```bash
md5sum [options] [arguments]
```

## Almindelige muligheder
- `-b`: Behandler binære filer.
- `-c`: Kontrollerer MD5-hash-værdier fra en fil.
- `-t`: Behandler tekstfiler.
- `--help`: Viser hjælp og tilgængelige muligheder.
- `--version`: Viser versionen af md5sum.

## Almindelige eksempler

1. **Beregn MD5-hash for en fil:**
   ```bash
   md5sum fil.txt
   ```

2. **Gem MD5-hash i en fil:**
   ```bash
   md5sum fil.txt > hash.txt
   ```

3. **Kontroller MD5-hash fra en fil:**
   ```bash
   md5sum -c hash.txt
   ```

4. **Beregn MD5-hash for flere filer:**
   ```bash
   md5sum fil1.txt fil2.txt fil3.txt
   ```

## Tips
- Brug `-c` optionen til at validere filer mod en tidligere gemt hash for at sikre, at de ikke er blevet ændret.
- Det er en god praksis at generere og gemme hash-værdier, når du overfører filer, for at kunne kontrollere integriteten senere.
- Vær opmærksom på, at MD5 ikke er den mest sikre hash-algoritme til kryptografiske formål, men den er hurtig og effektiv til dataintegritetstjek.