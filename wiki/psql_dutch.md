# [Linux] C Shell (csh) psql gebruik: Voer SQL-commando's uit op een PostgreSQL-database

## Overzicht
De `psql`-opdracht is een interactieve terminal voor het werken met PostgreSQL-databases. Het stelt gebruikers in staat om SQL-commando's uit te voeren, database-informatie op te vragen en databasebeheer uit te voeren.

## Gebruik
De basis syntaxis van de `psql`-opdracht is als volgt:

```csh
psql [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`: Specificeert de host van de database.
- `-U`: Geeft de gebruikersnaam op voor de databaseverbinding.
- `-d`: Bepaalt de naam van de database waarmee verbinding moet worden gemaakt.
- `-W`: Vraagt om een wachtwoord voor de opgegeven gebruiker.
- `-c`: Voert een enkele SQL-opdracht uit en sluit daarna af.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `psql`:

1. Verbinden met een lokale database:

   ```csh
   psql -U gebruikersnaam -d databasenaam
   ```

2. Een SQL-opdracht uitvoeren vanuit de opdrachtregel:

   ```csh
   psql -U gebruikersnaam -d databasenaam -c "SELECT * FROM tabelnaam;"
   ```

3. Verbinden met een database op een externe host:

   ```csh
   psql -h externe_host -U gebruikersnaam -d databasenaam
   ```

4. Een wachtwoord opgeven bij het verbinden:

   ```csh
   psql -U gebruikersnaam -d databasenaam -W
   ```

## Tips
- Zorg ervoor dat je de juiste gebruikersrechten hebt voor de database waarmee je verbinding maakt.
- Gebruik de `\?`-opdracht binnen `psql` om een lijst van beschikbare commando's en opties te bekijken.
- Maak gebruik van de `\q`-opdracht om `psql` veilig af te sluiten.