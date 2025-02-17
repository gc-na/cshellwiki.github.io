# [Linux] Bash fmt brug: Formaterer tekstfiler

## Oversigt
`fmt` er et kommandolinjeværktøj, der bruges til at formatere tekstfiler. Det justerer linjelængden i en tekst, så den bliver mere læsevenlig og ensartet. Dette kan være nyttigt, når man arbejder med tekstfiler, der har uregelmæssige linjelængder.

## Brug
Den grundlæggende syntaks for `fmt`-kommandoen er:

```bash
fmt [muligheder] [argumenter]
```

## Almindelige muligheder
- `-w, --width <num>`: Angiver den ønskede maksimale linjelængde (standard er 75 tegn).
- `-s, --split-only`: Deler kun linjer, der er længere end den angivne bredde, uden at ændre eksisterende linjer.
- `-u, --uniform`: Gør linjerne ensartede ved at justere dem til den angivne bredde.

## Almindelige eksempler

1. **Formatere en tekstfil til standard bredde:**
   ```bash
   fmt tekstfil.txt
   ```

2. **Formatere en tekstfil med en specifik linjelængde på 50 tegn:**
   ```bash
   fmt -w 50 tekstfil.txt
   ```

3. **Brug af split-only for at undgå ændringer af korte linjer:**
   ```bash
   fmt -s tekstfil.txt
   ```

4. **Gøre linjerne ensartede med en bredde på 60 tegn:**
   ```bash
   fmt -u -w 60 tekstfil.txt
   ```

## Tips
- Overvej at bruge `-w`-muligheden for at tilpasse linjelængden til dit specifikke behov.
- Kombiner `fmt` med andre værktøjer som `cat` eller `less` for bedre visning af formaterede filer.
- Test `fmt` på en kopi af dine filer for at undgå utilsigtede ændringer i originale dokumenter.