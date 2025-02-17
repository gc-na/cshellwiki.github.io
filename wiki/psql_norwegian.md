# [Linux] Bash psql bruk: Koble til og administrere PostgreSQL-databaser

## Oversikt
`psql` er kommandolinjeverktøyet for PostgreSQL, som lar brukere utføre SQL-spørringer, administrere databaser og interagere med PostgreSQL-servere. Det gir en interaktiv terminal for å utføre SQL-kommandoer og administrere databaser effektivt.

## Bruk
Grunnleggende syntaks for `psql`-kommandoen er som følger:

```bash
psql [alternativer] [argumenter]
```

## Vanlige alternativer
- `-h, --host=VERDI`: Angi verten til PostgreSQL-serveren.
- `-p, --port=VERDI`: Angi porten som serveren lytter på.
- `-U, --username=VERDI`: Angi brukernavnet for å koble til databasen.
- `-d, --dbname=VERDI`: Angi navnet på databasen du vil koble til.
- `-f, --file=FILNAVN`: Kjør SQL-kommandoer fra en fil.

## Vanlige eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `psql`:

1. Koble til en lokal PostgreSQL-database:
   ```bash
   psql -U brukernavn -d databasename
   ```

2. Koble til en PostgreSQL-database på en spesifikk vert og port:
   ```bash
   psql -h vert -p 5432 -U brukernavn -d databasename
   ```

3. Kjør SQL-kommandoer fra en fil:
   ```bash
   psql -U brukernavn -d databasename -f script.sql
   ```

4. Utfør en enkel SQL-spørring direkte fra kommandolinjen:
   ```bash
   psql -U brukernavn -d databasename -c "SELECT * FROM tabellnavn;"
   ```

## Tips
- Bruk `\q` for å avslutte `psql`-økten.
- Du kan bruke `\h` for å få hjelp til SQL-kommandoer.
- For å liste alle tilgjengelige databaser, bruk `\l` etter å ha koblet til `psql`.
- Lagre ofte brukte spørringer i en fil for enkel tilgang og kjøring.