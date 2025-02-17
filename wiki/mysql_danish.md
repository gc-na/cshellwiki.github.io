# [Linux] Bash mysql brug: Interagere med MySQL-databaser

## Overview
`mysql`-kommandoen er et kommandolinjeprogram, der bruges til at interagere med MySQL-databaser. Det giver brugerne mulighed for at udføre SQL-forespørgsler, administrere databaser og udføre forskellige administrative opgaver.

## Usage
Den grundlæggende syntaks for `mysql`-kommandoen er som følger:

```bash
mysql [options] [arguments]
```

## Common Options
Her er nogle almindelige muligheder for `mysql`-kommandoen:

- `-u, --user=name`: Angiv brugernavnet til MySQL-serveren.
- `-p, --password[=name]`: Angiv adgangskoden til MySQL-brugeren. Hvis adgangskoden ikke angives, vil systemet bede om den.
- `-h, --host=name`: Angiv værtsnavnet på MySQL-serveren (standard er localhost).
- `-D, --database=name`: Angiv den database, der skal bruges ved opstart.
- `--port=#`: Angiv portnummeret, som MySQL-serveren lytter på (standard er 3306).

## Common Examples
Her er nogle praktiske eksempler på brugen af `mysql`-kommandoen:

1. **Log ind på MySQL-serveren:**
   ```bash
   mysql -u root -p
   ```

2. **Log ind på en specifik database:**
   ```bash
   mysql -u root -p -D my_database
   ```

3. **Kør en SQL-forespørgsel fra kommandolinjen:**
   ```bash
   mysql -u root -p -e "SHOW DATABASES;"
   ```

4. **Importér en SQL-fil til en database:**
   ```bash
   mysql -u root -p my_database < backup.sql
   ```

5. **Eksportér en database til en SQL-fil:**
   ```bash
   mysqldump -u root -p my_database > backup.sql
   ```

## Tips
- Brug `--verbose` for at få mere detaljerede oplysninger om, hvad `mysql`-kommandoen gør.
- For at undgå at indtaste adgangskoden hver gang, kan du oprette en `.my.cnf`-fil i din hjemmemappe med dine loginoplysninger.
- Vær opmærksom på, at SQL-forespørgsler er case-sensitive, så vær konsekvent med brugen af store og små bogstaver.
- Brug `--help` for at få en liste over alle tilgængelige muligheder og syntaks for `mysql`-kommandoen.