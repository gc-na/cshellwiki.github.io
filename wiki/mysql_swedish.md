# [Linux] Bash mysql användning: Hantera MySQL-databaser

## Översikt
`mysql` är ett kommandoradsverktyg som används för att interagera med MySQL-databaser. Det gör det möjligt för användare att köra SQL-frågor, hantera databaser och utföra olika administrativa uppgifter direkt från terminalen.

## Användning
Den grundläggande syntaxen för kommandot är:

```bash
mysql [alternativ] [argument]
```

## Vanliga alternativ
- `-u, --user=USER` : Ange användarnamn för att logga in.
- `-p, --password[=PASSWORD]` : Ange lösenord för användaren (om inget lösenord anges, kommer du att uppmanas att ange det).
- `-h, --host=HOST` : Ange värdnamnet för MySQL-servern.
- `-D, --database=DB` : Ange databasen som ska användas vid inloggning.
- `-e, --execute=STATEMENT` : Kör en SQL-fråga direkt från kommandoraden.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `mysql`:

1. **Logga in på MySQL-servern:**
   ```bash
   mysql -u användarnamn -p
   ```

2. **Ansluta till en specifik databas:**
   ```bash
   mysql -u användarnamn -p -D databasnamn
   ```

3. **Köra en SQL-fråga direkt:**
   ```bash
   mysql -u användarnamn -p -e "SHOW DATABASES;"
   ```

4. **Exportera en databas till en fil:**
   ```bash
   mysqldump -u användarnamn -p databasnamn > backup.sql
   ```

5. **Importera en databas från en fil:**
   ```bash
   mysql -u användarnamn -p databasnamn < backup.sql
   ```

## Tips
- Använd `--verbose` för att få mer detaljerad information om vad kommandot gör.
- Om du ofta använder samma alternativ, överväg att skapa en `.my.cnf`-fil i din hemkatalog för att spara dina inställningar.
- Var försiktig med att dela lösenord i kommandoraden, eftersom det kan ses av andra användare på systemet. Använd istället `-p` utan att ange lösenordet direkt för att bli ombedd att ange det.