# [Linux] Bash printenv brug: Vise miljøvariabler

## Oversigt
`printenv`-kommandoen bruges til at vise miljøvariabler i et Bash-shell. Den giver en liste over alle de aktuelle miljøvariabler og deres værdier, hvilket kan være nyttigt til fejlfinding og konfiguration.

## Brug
Den grundlæggende syntaks for `printenv`-kommandoen er:

```bash
printenv [options] [arguments]
```

## Almindelige muligheder
- `-0`, `--null`: Skaber output, der adskilles med null-tegn i stedet for nye linjer. Dette kan være nyttigt til at håndtere variabler med nye linjer i deres værdier.
- `VARIABLE`: Angiv navnet på en specifik miljøvariabel for kun at vise dens værdi.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `printenv`:

1. **Vis alle miljøvariabler:**
   ```bash
   printenv
   ```

2. **Vis en specifik miljøvariabel (f.eks. PATH):**
   ```bash
   printenv PATH
   ```

3. **Vis miljøvariabler adskilt med null-tegn:**
   ```bash
   printenv -0
   ```

## Tips
- Brug `printenv` i kombination med `grep` for at filtrere specifikke variabler. For eksempel:
  ```bash
  printenv | grep USER
  ```
- Vær opmærksom på, at `printenv` kun viser variabler, der er tilgængelige i det aktuelle shell-miljø. For at se alle variabler, inklusive lokale, kan du bruge `set`-kommandoen.
- Hvis du kun vil se værdien af en variabel, kan du også bruge `echo`-kommandoen, f.eks. `echo $HOME`.