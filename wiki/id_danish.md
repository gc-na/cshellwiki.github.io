# [Linux] Bash id brug: Vis bruger- og gruppeinformation

## Overview
`id`-kommandoen bruges til at vise brugerens UID (User ID), GID (Group ID) og de grupper, som brugeren tilhører. Det er et nyttigt værktøj til at få indsigt i brugerens rettigheder og tilknytninger i systemet.

## Usage
Den grundlæggende syntaks for `id`-kommandoen er som følger:

```
id [options] [arguments]
```

## Common Options
- `-u`: Vis kun UID for den angivne bruger.
- `-g`: Vis kun GID for den angivne bruger.
- `-G`: Vis alle GIDs for den angivne bruger.
- `-n`: Vis navn i stedet for numerisk ID.
- `-r`: Vis den relative ID (kun for grupper).

## Common Examples
Her er nogle praktiske eksempler på, hvordan du kan bruge `id`-kommandoen:

1. **Vis din egen bruger- og gruppeinformation:**
   ```bash
   id
   ```

2. **Vis UID og GID for en specifik bruger:**
   ```bash
   id brugernavn
   ```

3. **Vis kun UID for den aktuelle bruger:**
   ```bash
   id -u
   ```

4. **Vis kun GID for den aktuelle bruger:**
   ```bash
   id -g
   ```

5. **Vis alle grupper, som en specifik bruger tilhører:**
   ```bash
   id -G brugernavn
   ```

## Tips
- Brug `id`-kommandoen i scripts for at kontrollere, om en bruger har de nødvendige rettigheder.
- Kombiner `id` med andre kommandoer som `grep` for at filtrere specifik information.
- Husk at bruge `-n` for at få navne i stedet for numeriske IDs, hvilket kan gøre output mere læsbart.