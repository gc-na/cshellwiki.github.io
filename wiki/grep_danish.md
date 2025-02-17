# [Linux] Bash grep brug: Søg i tekstfiler

## Oversigt
`grep` er et kraftfuldt værktøj i Bash, der bruges til at søge efter specifikke mønstre i tekstfiler. Det kan finde linjer, der matcher et givet mønster, hvilket gør det nyttigt til at filtrere og analysere data.

## Brug
Den grundlæggende syntaks for `grep` er som følger:

```bash
grep [muligheder] [argumenter]
```

## Almindelige muligheder
- `-i`: Ignorerer forskelle i store og små bogstaver.
- `-v`: Viser linjer, der ikke matcher mønsteret.
- `-r`: Søg rekursivt i alle filer i en mappe.
- `-n`: Viser linjenumre for hver match.
- `-l`: Viser kun filnavne, der indeholder et match.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `grep` kan bruges:

1. **Søg efter et ord i en fil:**
   ```bash
   grep "ord" fil.txt
   ```

2. **Søg efter et ord uden at tage højde for store og små bogstaver:**
   ```bash
   grep -i "ord" fil.txt
   ```

3. **Vis linjer, der ikke indeholder et bestemt ord:**
   ```bash
   grep -v "ord" fil.txt
   ```

4. **Søg rekursivt i en mappe:**
   ```bash
   grep -r "ord" /sti/til/mappe
   ```

5. **Vis linjenumre for hver match:**
   ```bash
   grep -n "ord" fil.txt
   ```

## Tips
- Brug `grep` sammen med andre kommandoer ved hjælp af pipe (`|`) for at filtrere output. For eksempel:
  ```bash
  dmesg | grep "fejl"
  ```
- For at søge i flere filer, kan du bruge jokertegn:
  ```bash
  grep "ord" *.txt
  ```
- Gem ofte brugte søgninger i et script for at automatisere processen.