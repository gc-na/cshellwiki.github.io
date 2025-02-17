# [Linux] Bash sha512sum brug: Beregn SHA-512 hash-værdier

## Oversigt
`sha512sum` er et Bash-kommando, der bruges til at generere SHA-512 hash-værdier for filer. Det er nyttigt til at kontrollere integriteten af filer ved at sammenligne hash-værdier.

## Brug
Den grundlæggende syntaks for `sha512sum`-kommandoen er:

```bash
sha512sum [options] [arguments]
```

## Almindelige muligheder
- `-b`: Behandler filen som binær.
- `-c`: Kontrollerer hash-værdierne mod en liste i en fil.
- `-h`: Viser hjælp og information om kommandoen.
- `--quiet`: Undertrykker output, hvis der ikke er fejl.

## Almindelige eksempler

1. **Generere en SHA-512 hash for en fil:**
   ```bash
   sha512sum fil.txt
   ```

2. **Gemme hash-værdien i en fil:**
   ```bash
   sha512sum fil.txt > hash.txt
   ```

3. **Kontrollere hash-værdier fra en fil:**
   ```bash
   sha512sum -c hash.txt
   ```

4. **Generere hash for flere filer:**
   ```bash
   sha512sum fil1.txt fil2.txt fil3.txt
   ```

## Tips
- Brug `-c`-muligheden for at validere filer mod en tidligere gemt hash-værdi.
- For at sikre, at du arbejder med de korrekte filer, kan du altid kontrollere hash-værdien efter at have overført eller ændret filer.
- Overvej at bruge `-b`-muligheden, hvis du arbejder med binære filer for at undgå problemer med filformater.