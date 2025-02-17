# [Linux] Bash kommando comm: Sammenlign to sorterede filer

## Oversigt
Kommandoen `comm` bruges til at sammenligne to sorterede filer linje for linje. Den viser de linjer, der er unikke for hver fil samt de linjer, der er fælles for begge filer. Dette er nyttigt, når du vil finde forskelle mellem to datasæt.

## Brug
Den grundlæggende syntaks for `comm` er som følger:

```bash
comm [options] [file1] [file2]
```

## Almindelige muligheder
- `-1`: Undertrykker output af linjer, der kun findes i den første fil.
- `-2`: Undertrykker output af linjer, der kun findes i den anden fil.
- `-3`: Undertrykker output af linjer, der findes i begge filer.
- `-i`: Ignorerer forskelle i store og små bogstaver.

## Almindelige eksempler

1. **Sammenlign to filer**:
   For at sammenligne to sorterede filer, `file1.txt` og `file2.txt`, kan du bruge:
   ```bash
   comm file1.txt file2.txt
   ```

2. **Vis kun linjer, der er unikke for den første fil**:
   Hvis du kun vil se linjer, der kun findes i `file1.txt`, kan du bruge:
   ```bash
   comm -13 file1.txt file2.txt
   ```

3. **Vis kun fælles linjer**:
   For kun at vise de linjer, der er fælles for begge filer, kan du bruge:
   ```bash
   comm -12 file1.txt file2.txt
   ```

4. **Ignorer store og små bogstaver**:
   Hvis du vil sammenligne to filer uden at tage hensyn til store og små bogstaver, kan du bruge:
   ```bash
   comm -i file1.txt file2.txt
   ```

## Tips
- Sørg for, at filerne er sorterede, før du bruger `comm`, da kommandoen kun fungerer korrekt med sorterede input.
- Du kan kombinere flere muligheder for at tilpasse outputtet til dine behov.
- Brug `sort`-kommandoen til at sortere filer, hvis de ikke allerede er sorterede:
  ```bash
  sort file1.txt > sorted_file1.txt
  sort file2.txt > sorted_file2.txt
  comm sorted_file1.txt sorted_file2.txt
  ```