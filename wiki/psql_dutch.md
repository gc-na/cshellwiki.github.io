# [Linux] Bash psql gebruik: Voer SQL-commando's uit op PostgreSQL-databases

## Overzicht
De `psql`-opdracht is een krachtige commandoregelinterface voor het interactief uitvoeren van SQL-commando's op PostgreSQL-databases. Het stelt gebruikers in staat om verbinding te maken met een database, queries uit te voeren en de resultaten te beheren.

## Gebruik
De basis syntaxis van de `psql`-opdracht is als volgt:

```bash
psql [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`: Specificeer de host waar de database draait.
- `-p`: Geef de poort op die gebruikt moet worden voor de verbinding.
- `-U`: Geef de gebruikersnaam op voor de databaseverbinding.
- `-d`: Geef de naam van de database op waarmee verbinding moet worden gemaakt.
- `-f`: Voer een SQL-bestand uit.

## Veelvoorkomende Voorbeelden
1. Verbinden met een database:
   ```bash
   psql -U gebruikersnaam -d databasenaam
   ```

2. Een SQL-bestand uitvoeren:
   ```bash
   psql -U gebruikersnaam -d databasenaam -f pad/naar/bestand.sql
   ```

3. Een eenvoudige SQL-query uitvoeren:
   ```bash
   psql -U gebruikersnaam -d databasenaam -c "SELECT * FROM tabelnaam;"
   ```

4. Verbinden met een specifieke host en poort:
   ```bash
   psql -h localhost -p 5432 -U gebruikersnaam -d databasenaam
   ```

## Tips
- Gebruik de `\?` commando binnen `psql` om een lijst van beschikbare commando's en hun beschrijvingen te krijgen.
- Maak gebruik van de `\q` om de `psql`-sessie veilig af te sluiten.
- Overweeg om een `.pgpass`-bestand te gebruiken om wachtwoorden op te slaan, zodat je niet telkens om een wachtwoord hoeft te vragen bij het verbinden.