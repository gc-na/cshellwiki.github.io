# [Linux] Bash fold brug: Formaterer tekst til specifik bredde

## Oversigt
`fold`-kommandoen bruges til at formatere tekst ved at bryde linjer, så de ikke overstiger en bestemt bredde. Dette er nyttigt, når man arbejder med tekstfiler, der skal vises på en skærm med begrænset plads eller når man ønsker at forberede tekst til udskrift.

## Brug
Den grundlæggende syntaks for `fold`-kommandoen er:

```bash
fold [muligheder] [argumenter]
```

## Almindelige muligheder
- `-w, --width=NUM`: Angiver den maksimale bredde af linjer i output. Standardbredden er 80 tegn.
- `-s, --spaces`: Bryder linjer ved det nærmeste mellemrum, hvis muligt, i stedet for midt i et ord.
- `-b, --bytes`: Angiver, at bredden skal måles i bytes i stedet for tegn.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `fold`:

1. **Standard brug**:
   For at formatere en tekstfil til standardbredde (80 tegn):
   ```bash
   fold myfile.txt
   ```

2. **Angive en specifik bredde**:
   For at formatere en tekstfil til 50 tegn pr. linje:
   ```bash
   fold -w 50 myfile.txt
   ```

3. **Brud ved mellemrum**:
   For at bryde linjer ved det nærmeste mellemrum:
   ```bash
   fold -s -w 50 myfile.txt
   ```

4. **Måle i bytes**:
   For at formatere en fil og måle bredden i bytes:
   ```bash
   fold -b -w 50 myfile.txt
   ```

## Tips
- Brug `-s`-muligheden, når du vil undgå at bryde ord, hvilket kan gøre output mere læsbart.
- Kombiner `fold` med andre kommandoer som `cat` eller `echo` for at formatere tekst direkte fra kommandolinjen.
- Overvej at bruge `fold` i scripts til at generere pænt formateret tekstoutput, især når du arbejder med logfiler eller rapporter.