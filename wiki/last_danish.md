# [Linux] Bash last brug: Vis brugeres loginhistorik

## Overview
`last` er en Bash-kommando, der bruges til at vise en liste over brugere, der har logget ind på systemet, samt oplysninger om deres login-sessioner. Det giver en nyttig oversigt over, hvornår brugere har været aktive og kan hjælpe med at overvåge systemadgang.

## Usage
Den grundlæggende syntaks for `last`-kommandoen er:

```bash
last [options] [arguments]
```

## Common Options
- `-a`: Viser den sidste loginadresse for hver bruger.
- `-n [number]`: Angiver, hvor mange login-sessioner der skal vises. Standard er at vise alle.
- `-x`: Viser også systemopstart og nedlukninger.
- `-R`: Udelukker visningen af værtsnavne.

## Common Examples
Her er nogle praktiske eksempler på brugen af `last`:

1. **Vis alle login-sessioner:**
   ```bash
   last
   ```

2. **Vis de sidste 5 login-sessioner:**
   ```bash
   last -n 5
   ```

3. **Vis login-sessioner med IP-adresser:**
   ```bash
   last -a
   ```

4. **Vis login-sessioner og systemopstart:**
   ```bash
   last -x
   ```

5. **Vis login-sessioner uden værtsnavne:**
   ```bash
   last -R
   ```

## Tips
- Brug `last` regelmæssigt for at overvåge brugernes aktivitet og sikre, at der ikke er uautoriseret adgang.
- Kombiner `last` med `grep` for at filtrere resultaterne, f.eks. for at finde login-sessioner for en bestemt bruger:
  ```bash
  last | grep username
  ```
- Vær opmærksom på, at `last` læser fra `/var/log/wtmp`, så hvis logfilerne er blevet ryddet, vil tidligere login-sessioner ikke være tilgængelige.