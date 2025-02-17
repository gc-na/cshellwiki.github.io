# [Linux] Bash ls brug: Liste filer og mapper

## Oversigt
`ls`-kommandoen bruges til at liste indholdet af en mappe. Den viser filer og undermapper i den angivne katalog og kan tilpasses med forskellige muligheder for at ændre, hvordan informationen præsenteres.

## Brug
Den grundlæggende syntaks for `ls`-kommandoen er:

```bash
ls [muligheder] [argumenter]
```

## Almindelige muligheder
- `-l`: Viser detaljeret information om filer og mapper, herunder rettigheder, ejer, størrelse og dato for seneste ændring.
- `-a`: Viser alle filer, inklusive skjulte filer, der starter med punktum (.)
- `-h`: Gør filstørrelser mere læselige ved at vise dem i kilobytes (K), megabytes (M) osv. (kan kun bruges med `-l`).
- `-R`: Viser filer i undermapper rekursivt.
- `-t`: Sorterer filer efter ændringsdato, så de nyeste filer vises først.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan `ls` kan bruges:

1. Liste filer i den nuværende mappe:
   ```bash
   ls
   ```

2. Liste alle filer, inklusive skjulte:
   ```bash
   ls -a
   ```

3. Liste filer med detaljeret information:
   ```bash
   ls -l
   ```

4. Liste filer med detaljeret information og læsbare størrelser:
   ```bash
   ls -lh
   ```

5. Liste filer sorteret efter ændringsdato:
   ```bash
   ls -lt
   ```

6. Liste filer rekursivt i alle undermapper:
   ```bash
   ls -R
   ```

## Tips
- Brug `ls` sammen med `| less` for at navigere i lange lister:
  ```bash
  ls -l | less
  ```
- Kombiner muligheder for at få den ønskede visning. For eksempel, for at se alle filer med detaljeret information og læsbare størrelser:
  ```bash
  ls -lha
  ```
- Husk, at `ls` sorterer filer alfabetisk som standard. Hvis du vil ændre sorteringen, kan du bruge `-t` eller `-S` for at sortere efter tid eller størrelse henholdsvis.