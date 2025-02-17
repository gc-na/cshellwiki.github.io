# [Linux] Bash head brug: Vis de første linjer af en fil

## Overview
`head`-kommandoen bruges til at vise de første linjer af en eller flere filer. Det er nyttigt, når du hurtigt vil se indholdet af en fil uden at åbne den helt.

## Usage
Den grundlæggende syntaks for `head`-kommandoen er:

```bash
head [options] [arguments]
```

## Common Options
- `-n [antal]`: Angiver antallet af linjer, der skal vises. Standard er 10 linjer.
- `-c [antal]`: Viser et bestemt antal bytes fra starten af filen.
- `-q`: Undertrykker overskrifterne for flere filer.
- `-v`: Viser overskrifterne for hver fil, selvom der kun vises én fil.

## Common Examples
Her er nogle praktiske eksempler på, hvordan du kan bruge `head`:

1. **Vis de første 10 linjer af en fil:**
   ```bash
   head filnavn.txt
   ```

2. **Vis de første 5 linjer af en fil:**
   ```bash
   head -n 5 filnavn.txt
   ```

3. **Vis de første 100 bytes af en fil:**
   ```bash
   head -c 100 filnavn.txt
   ```

4. **Vis de første 10 linjer af flere filer:**
   ```bash
   head fil1.txt fil2.txt
   ```

5. **Vis de første 10 linjer og inkluder overskrifter:**
   ```bash
   head -v fil1.txt fil2.txt
   ```

## Tips
- Brug `head` i kombination med `tail` for at se et specifikt udsnit af en fil.
- Hvis du kun vil se en del af en stor fil, kan du kombinere `head` med `grep` for at filtrere indholdet.
- Husk at `head` ikke ændrer filen; det viser kun indholdet i terminalen.