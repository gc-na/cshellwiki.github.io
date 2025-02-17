# [Linux] Bash zip brug: Komprimerer filer og mapper

## Oversigt
`zip` er et kommandolinjeværktøj, der bruges til at komprimere filer og mapper til et enkelt zip-arkiv. Dette gør det lettere at opbevare og overføre flere filer på én gang.

## Brug
Den grundlæggende syntaks for `zip`-kommandoen er:

```bash
zip [muligheder] [arkivnavn.zip] [filer/mapper]
```

## Almindelige muligheder
- `-r`: Rekursivt komprimere mapper og deres indhold.
- `-e`: Krypter zip-arkivet med en adgangskode.
- `-u`: Opdater eksisterende filer i arkivet.
- `-d`: Slet filer fra zip-arkivet.
- `-l`: Vis indholdet af zip-arkivet.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `zip`-kommandoen:

1. **Oprette et zip-arkiv fra filer:**
   ```bash
   zip minefiler.zip fil1.txt fil2.txt fil3.txt
   ```

2. **Rekursivt komprimere en mappe:**
   ```bash
   zip -r minmappe.zip /sti/til/mappe
   ```

3. **Kryptere et zip-arkiv:**
   ```bash
   zip -e sikret.zip fil1.txt fil2.txt
   ```

4. **Opdatere et eksisterende zip-arkiv:**
   ```bash
   zip -u minefiler.zip fil4.txt
   ```

5. **Slette en fil fra et zip-arkiv:**
   ```bash
   zip -d minefiler.zip fil2.txt
   ```

## Tips
- Brug `-r` muligheden, når du komprimerer mapper for at sikre, at alle underliggende filer inkluderes.
- Overvej at bruge kryptering med `-e`, hvis du håndterer følsomme oplysninger.
- For at se indholdet af et zip-arkiv uden at udpakke det, kan du bruge `unzip -l arkivnavn.zip`.