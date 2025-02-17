# [Linux] Bash logout brug: Afslut en shell-session

## Overview
`logout`-kommandoen bruges til at afslutte en aktiv shell-session. Det er en nyttig kommando, når du ønsker at logge ud fra en terminal eller en SSH-session.

## Usage
Den grundlæggende syntaks for `logout`-kommandoen er:

```bash
logout [options]
```

## Common Options
Der er ikke mange muligheder for `logout`, da det primært er en simpel kommando. Den bruges typisk uden yderligere indstillinger. 

## Common Examples
Her er nogle praktiske eksempler på brugen af `logout`:

1. **Afslutning af en interaktiv shell-session:**
   ```bash
   logout
   ```

2. **Afslutning af en SSH-session:**
   Når du er logget ind på en fjernserver via SSH, kan du afslutte sessionen ved at skrive:
   ```bash
   logout
   ```

3. **Afslutning af en subshell:**
   Hvis du har åbnet en subshell, kan du afslutte den ved at bruge:
   ```bash
   logout
   ```

## Tips
- Sørg for at gemme dit arbejde, før du bruger `logout`, da det vil afslutte din session uden at spørge om bekræftelse.
- Hvis du bruger `logout` i en grafisk terminal, kan du også overveje at bruge `exit`-kommandoen, som fungerer på samme måde.
- Hvis du er i en skriptfil, skal du være opmærksom på, at `logout` kun fungerer i interaktive shell-sessioner.