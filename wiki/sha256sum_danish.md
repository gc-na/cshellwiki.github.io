# [Linux] Bash sha256sum brug: Beregn SHA-256 hash-værdier

## Oversigt
`sha256sum` er et Bash-kommando, der bruges til at beregne og verificere SHA-256 hash-værdier af filer. Denne kommando er nyttig til at sikre integriteten af data ved at generere en unik hash-værdi for en given fil.

## Brug
Den grundlæggende syntaks for `sha256sum` er:

```bash
sha256sum [options] [arguments]
```

## Almindelige muligheder
- `-b`, `--binary`: Behandler input som binært.
- `-c`, `--check`: Kontrollerer hash-værdierne mod en given fil.
- `-h`, `--help`: Viser hjælp og information om kommandoen.
- `-o`, `--output`: Angiver en fil til at skrive output til.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `sha256sum`:

1. **Beregn hash-værdien af en fil:**
   ```bash
   sha256sum fil.txt
   ```

2. **Gem hash-værdien i en fil:**
   ```bash
   sha256sum fil.txt > hash.txt
   ```

3. **Kontroller hash-værdier fra en fil:**
   ```bash
   sha256sum -c hash.txt
   ```

4. **Beregn hash-værdien af flere filer:**
   ```bash
   sha256sum fil1.txt fil2.txt
   ```

## Tips
- Brug `-c` muligheden til at verificere filer mod en tidligere gemt hash-værdi for at sikre, at de ikke er blevet ændret.
- Det kan være nyttigt at gemme hash-værdier i en tekstfil, så du nemt kan kontrollere dem senere.
- Vær opmærksom på, at selv en lille ændring i filen vil resultere i en helt anden hash-værdi.