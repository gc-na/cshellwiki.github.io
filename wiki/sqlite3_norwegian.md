# [Linux] Bash sqlite3 Bruk: Interagere med SQLite-databaser

## Oversikt
`sqlite3` er et kommandolinjeverktøy som brukes til å interagere med SQLite-databaser. Det lar brukere opprette, administrere og forespørre databaser på en enkel måte.

## Bruk
Den grunnleggende syntaksen for `sqlite3`-kommandoen er som følger:

```bash
sqlite3 [alternativer] [argumenter]
```

## Vanlige Alternativer
- `-help`: Viser hjelp og tilgjengelige alternativer.
- `-version`: Viser versjonen av sqlite3.
- `-init <fil>`: Kjør kommandoer fra en spesifisert fil ved oppstart.
- `-batch`: Kjør i batch-modus, uten interaktivt grensesnitt.
- `-cmd <kommando>`: Kjør en spesifisert kommando før du går inn i interaktiv modus.

## Vanlige Eksempler
Her er noen praktiske eksempler på hvordan du kan bruke `sqlite3`:

### Opprette en ny database
```bash
sqlite3 min_database.db
```

### Opprette en tabell
```bash
sqlite3 min_database.db "CREATE TABLE brukere (id INTEGER PRIMARY KEY, navn TEXT);"
```

### Legge til data i tabellen
```bash
sqlite3 min_database.db "INSERT INTO brukere (navn) VALUES ('Ola');"
```

### Hente data fra tabellen
```bash
sqlite3 min_database.db "SELECT * FROM brukere;"
```

### Slette databasen
```bash
rm min_database.db
```

## Tips
- Bruk `-init` for å kjøre en skriptfil med SQL-kommandoer for å sette opp databasen raskt.
- Husk å bruke `-batch` når du kjører skript for å unngå interaktive spørsmål.
- Lag sikkerhetskopier av databasen regelmessig for å unngå datatap.