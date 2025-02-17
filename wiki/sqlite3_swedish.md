# [Linux] Bash sqlite3 användning: Interagera med SQLite-databaser

## Översikt
Kommandot `sqlite3` används för att interagera med SQLite-databaser. Det gör det möjligt att skapa, läsa, uppdatera och ta bort data i en SQLite-databas via kommandoraden.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
sqlite3 [alternativ] [argument]
```

## Vanliga alternativ
- `-help`: Visar hjälpmeddelande med tillgängliga alternativ.
- `-version`: Visar versionen av sqlite3.
- `-init <fil>`: Initierar databasen med SQL-kommandon från den angivna filen.
- `<databas>`: Namnet på databasen som ska öppnas eller skapas.

## Vanliga exempel
Här är några praktiska exempel på hur du kan använda `sqlite3`:

### Skapa en ny databas
```bash
sqlite3 min_databas.db
```

### Skapa en tabell
```bash
sqlite3 min_databas.db "CREATE TABLE användare (id INTEGER PRIMARY KEY, namn TEXT, ålder INTEGER);"
```

### Infoga data i tabellen
```bash
sqlite3 min_databas.db "INSERT INTO användare (namn, ålder) VALUES ('Anna', 30);"
```

### Hämta data från tabellen
```bash
sqlite3 min_databas.db "SELECT * FROM användare;"
```

### Ta bort en tabell
```bash
sqlite3 min_databas.db "DROP TABLE användare;"
```

## Tips
- Använd `-init` för att köra en SQL-fil med flera kommandon för att snabbt ställa in databasen.
- Kom ihåg att avsluta SQL-kommandon med ett semikolon (`;`).
- Du kan använda `.exit` för att avsluta sqlite3-prompten.
- Använd `-header` för att visa kolumnnamn i resultaten när du kör SELECT-frågor.