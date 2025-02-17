# [Linux] Bash sqlite3 brug: Interagere med SQLite databaser

## Oversigt
`sqlite3` er et kommandolinjeværktøj, der bruges til at interagere med SQLite-databaser. Det giver brugerne mulighed for at udføre SQL-forespørgsler, administrere databaser og manipulere data direkte fra terminalen.

## Brug
Den grundlæggende syntaks for `sqlite3`-kommandoen er:

```bash
sqlite3 [muligheder] [argumenter]
```

## Almindelige muligheder
- `-help`: Viser hjælp og tilgængelige kommandoer.
- `-version`: Viser versionen af sqlite3.
- `-init <fil>`: Kører SQL-kommandoer fra den angivne fil ved opstart.
- `-batch`: Kører i batch-tilstand, hvilket betyder, at output ikke formateres.
- `-readonly`: Åbner databasen i skrivebeskyttet tilstand.

## Almindelige eksempler
Her er nogle praktiske eksempler på, hvordan man bruger `sqlite3`:

1. **Oprette en ny database**:
   ```bash
   sqlite3 min_database.db
   ```

2. **Køre en SQL-kommando**:
   ```bash
   sqlite3 min_database.db "CREATE TABLE brugere (id INTEGER PRIMARY KEY, navn TEXT);"
   ```

3. **Indsætte data i en tabel**:
   ```bash
   sqlite3 min_database.db "INSERT INTO brugere (navn) VALUES ('Alice');"
   ```

4. **Hente data fra en tabel**:
   ```bash
   sqlite3 min_database.db "SELECT * FROM brugere;"
   ```

5. **Køre SQL-kommandoer fra en fil**:
   ```bash
   sqlite3 min_database.db < mine_kommandoer.sql
   ```

## Tips
- Brug `-init` til at køre en række SQL-kommandoer automatisk, når du åbner databasen.
- For at undgå at miste data, skal du altid tage backup af din database, før du foretager ændringer.
- Udnyt batch-tilstand, hvis du har mange forespørgsler, da det kan forbedre ydeevnen ved at minimere output.