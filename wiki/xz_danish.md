# [Linux] Bash xz Brug: Komprimering af filer

## Oversigt
`xz` er et kommandolinjeværktøj til komprimering af filer ved hjælp af LZMA-algoritmen. Det er kendt for at skabe meget små komprimerede filer, hvilket gør det ideelt til at reducere filstørrelser og spare plads.

## Brug
Den grundlæggende syntaks for `xz`-kommandoen er som følger:

```bash
xz [muligheder] [argumenter]
```

## Almindelige muligheder
- `-d`, `--decompress`: Dekomprimerer en fil.
- `-k`, `--keep`: Beholder den originale fil efter komprimering.
- `-f`, `--force`: Tvinger komprimering eller dekomprimering, selvom det kan overskrive eksisterende filer.
- `-z`, `--compress`: Komprimerer en fil (standard handling).
- `-9`: Angiver den højeste komprimeringsniveau (1-9, hvor 9 er mest komprimering).

## Almindelige eksempler
- Komprimere en fil:
  ```bash
  xz fil.txt
  ```
  
- Dekomprimere en fil:
  ```bash
  xz -d fil.txt.xz
  ```

- Komprimere en fil og bevare den originale:
  ```bash
  xz -k fil.txt
  ```

- Tvinge komprimering af en fil, selv hvis den allerede findes:
  ```bash
  xz -f fil.txt
  ```

- Komprimere en fil med det højeste komprimeringsniveau:
  ```bash
  xz -9 fil.txt
  ```

## Tips
- Brug `-k` muligheden, hvis du vil beholde den originale fil, indtil du er sikker på, at komprimeringen er vellykket.
- Overvej at bruge `-d` med `-k` for at dekomprimere og samtidig bevare den komprimerede fil.
- For batch-komprimering kan du bruge jokertegn, som i `xz *.txt` for at komprimere alle tekstfiler i den aktuelle mappe.