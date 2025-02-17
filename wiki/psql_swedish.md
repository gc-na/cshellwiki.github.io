# [Linux] Bash psql användning: Interagera med PostgreSQL-databaser

## Översikt
`psql` är en kommandoradsgränssnitt för att interagera med PostgreSQL-databaser. Det tillåter användare att köra SQL-frågor, hantera databaser och utföra olika administrativa uppgifter direkt från terminalen.

## Användning
Den grundläggande syntaxen för `psql` är:

```bash
psql [alternativ] [argument]
```

## Vanliga alternativ
- `-h`: Anger värden för databasservern.
- `-U`: Anger användarnamnet för att logga in.
- `-d`: Anger namnet på databasen att ansluta till.
- `-p`: Anger portnumret för att ansluta till databasservern.
- `-f`: Kör SQL-kommandon från en fil.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `psql`:

1. Anslut till en databas:
   ```bash
   psql -U användarnamn -d databasnamn
   ```

2. Anslut till en databas på en specifik värd och port:
   ```bash
   psql -h localhost -p 5432 -U användarnamn -d databasnamn
   ```

3. Kör en SQL-fil:
   ```bash
   psql -U användarnamn -d databasnamn -f /sökväg/till/fil.sql
   ```

4. Utför en enkel SQL-fråga direkt från kommandoraden:
   ```bash
   psql -U användarnamn -d databasnamn -c "SELECT * FROM tabellnamn;"
   ```

## Tips
- Använd `\?` inom `psql` för att få en lista över tillgängliga kommandon och alternativ.
- För att avsluta `psql`, skriv `\q` och tryck på Enter.
- Använd `\l` för att lista alla databaser och `\c databasnamn` för att byta till en annan databas.
- Tänk på att använda `-W` för att uppmanas att ange lösenord, vilket ökar säkerheten vid inloggning.