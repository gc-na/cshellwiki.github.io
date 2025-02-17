# [Linux] Bash wc brug: Tæller linjer, ord og tegn i filer

## Oversigt
`wc` (word count) er en Bash-kommando, der bruges til at tælle linjer, ord og tegn i en eller flere filer. Det er et nyttigt værktøj til hurtigt at få indsigt i indholdet af tekstfiler.

## Brug
Den grundlæggende syntaks for `wc`-kommandoen er som følger:

```bash
wc [muligheder] [argumenter]
```

## Almindelige muligheder
- `-l`: Tæller antallet af linjer.
- `-w`: Tæller antallet af ord.
- `-c`: Tæller antallet af tegn.
- `-m`: Tæller antallet af tegn (inklusive multibyte-tegn).
- `-L`: Viser længden af den længste linje.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `wc`:

1. Tæl linjerne i en fil:
   ```bash
   wc -l filnavn.txt
   ```

2. Tæl ordene i en fil:
   ```bash
   wc -w filnavn.txt
   ```

3. Tæl tegnene i en fil:
   ```bash
   wc -c filnavn.txt
   ```

4. Tæl linjer, ord og tegn i en fil samtidig:
   ```bash
   wc filnavn.txt
   ```

5. Tæl linjerne i flere filer:
   ```bash
   wc -l fil1.txt fil2.txt
   ```

## Tips
- Brug `wc` i kombination med andre kommandoer ved hjælp af en pipe (`|`) for at analysere output fra dem. For eksempel:
  ```bash
  ls | wc -l
  ```
  Dette tæller antallet af filer i den aktuelle mappe.
  
- Hvis du arbejder med store filer, kan det være nyttigt at bruge `-l` eller `-w` alene for at få hurtigere resultater.
  
- Husk at `wc` kan håndtere flere filer på én gang, hvilket gør det nemt at få en samlet tælling.