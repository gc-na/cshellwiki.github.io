# [Linux] Bash psql brug: Interagere med PostgreSQL databaser

## Oversigt
`psql` er en kommandolinjegrænseflade til at interagere med PostgreSQL databaser. Det giver brugerne mulighed for at udføre SQL-forespørgsler, administrere databaser og udføre forskellige administrative opgaver direkte fra terminalen.

## Brug
Den grundlæggende syntaks for `psql`-kommandoen er som følger:

```bash
psql [muligheder] [argumenter]
```

## Almindelige muligheder
- `-h` : Angiv værtsnavn for databasen.
- `-p` : Angiv portnummer for databasen.
- `-U` : Angiv brugernavnet til databasen.
- `-d` : Angiv navnet på databasen, der skal forbindes til.
- `-c` : Udfør en enkelt SQL-kommando og afslut.
- `-f` : Udfør SQL-kommandoer fra en fil.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `psql`:

1. Forbind til en lokal database med standardindstillinger:
   ```bash
   psql -d min_database
   ```

2. Forbind til en database på en specifik værtsmaskine:
   ```bash
   psql -h localhost -U min_bruger -d min_database
   ```

3. Udfør en SQL-kommando direkte fra kommandolinjen:
   ```bash
   psql -d min_database -c "SELECT * FROM min_tabel;"
   ```

4. Udfør SQL-kommandoer fra en fil:
   ```bash
   psql -d min_database -f script.sql
   ```

## Tips
- Brug `\q` for at afslutte `psql`-sessionen.
- Du kan bruge `\l` for at liste alle databaser og `\dt` for at vise alle tabeller i den aktuelle database.
- Gem ofte brugte SQL-kommandoer i en fil, så du hurtigt kan køre dem med `-f`-muligheden.
- Overvej at bruge `.pgpass`-filen til at gemme dine adgangskoder sikkert, så du ikke behøver at indtaste dem hver gang.