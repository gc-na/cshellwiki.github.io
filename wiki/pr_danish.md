# [Linux] Bash pr: Formaterer tekstfiler til udskrift

## Oversigt
`pr`-kommandoen bruges til at formatere tekstfiler, så de er lettere at læse og udskrive. Den opdeler indholdet i kolonner og tilføjer overskrifter og sidehoved, hvilket gør det ideelt til at forberede dokumenter til udskrift.

## Brug
Den grundlæggende syntaks for `pr`-kommandoen er:

```bash
pr [muligheder] [argumenter]
```

## Almindelige muligheder
- `-h, --header <header>`: Angiver en brugerdefineret overskrift for udskriften.
- `-n, --no-header`: Deaktiverer standard overskrifter.
- `-t, --omit-header`: Udelader overskrifter og sidefødder.
- `-s, --separator <tegn>`: Angiver et separator-tegn mellem kolonner.
- `-w, --width <bredde>`: Angiver bredden på udskriften i tegn.

## Almindelige eksempler
Her er nogle praktiske eksempler på brugen af `pr`:

1. **Formatere en tekstfil til udskrift med standardindstillinger:**
   ```bash
   pr fil.txt
   ```

2. **Tilføje en brugerdefineret overskrift:**
   ```bash
   pr -h "Min Overskrift" fil.txt
   ```

3. **Udelade standard overskrifter:**
   ```bash
   pr -n fil.txt
   ```

4. **Formatere en fil med flere kolonner og en specifik separator:**
   ```bash
   pr -s "," -w 80 fil.txt
   ```

5. **Oprette en side med flere kolonner:**
   ```bash
   pr -m fil1.txt fil2.txt
   ```

## Tips
- Brug `pr` sammen med `lp` eller `lpr` for direkte at sende den formaterede udskrift til printeren.
- Eksperimenter med forskellige muligheder for at finde den bedste formatering til dit dokument.
- Tjek filens indhold med `cat` eller `less` før du bruger `pr`, så du kan se, hvordan det vil blive formateret.