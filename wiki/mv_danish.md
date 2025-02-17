# [Linux] Bash mv brug: Flyt eller omdøb filer og mapper

## Oversigt
`mv`-kommandoen bruges til at flytte eller omdøbe filer og mapper i Linux. Det er en grundlæggende kommando, der er uundgåelig for filhåndtering i terminalen.

## Brug
Den grundlæggende syntaks for `mv`-kommandoen er som følger:

```bash
mv [muligheder] [argumenter]
```

## Almindelige muligheder
- `-i`: Spørg før overskrivning af en eksisterende fil.
- `-u`: Flyt kun, hvis kildefilen er nyere end destinationsfilen eller hvis destinationsfilen ikke findes.
- `-v`: Vis detaljer om, hvad der bliver flyttet eller omdøbt.
- `-n`: Overskriv ikke eksisterende filer.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `mv`-kommandoen:

1. **Flyt en fil til en anden mappe:**
   ```bash
   mv fil.txt /sti/til/mappen/
   ```

2. **Omdøb en fil:**
   ```bash
   mv gammel_fil.txt ny_fil.txt
   ```

3. **Flyt flere filer til en mappe:**
   ```bash
   mv fil1.txt fil2.txt /sti/til/mappen/
   ```

4. **Brug af -i for at undgå utilsigtet overskrivning:**
   ```bash
   mv -i fil.txt /sti/til/mappen/
   ```

5. **Vis detaljer om flytningen:**
   ```bash
   mv -v fil.txt /sti/til/mappen/
   ```

## Tips
- Brug `-i`-muligheden for at undgå at overskrive filer ved et uheld.
- Tjek altid, at du har de korrekte stier, især når du arbejder med vigtige filer.
- Hvis du flytter mange filer, kan det være nyttigt at bruge `-v` for at se, hvad der sker undervejs.