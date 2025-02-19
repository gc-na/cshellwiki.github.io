# [Linux] C Shell (csh) mysql gebruik: Beheer van MySQL-databases

## Overzicht
De `mysql`-opdracht is een commandoregelinterface voor het communiceren met MySQL-databases. Het stelt gebruikers in staat om SQL-query's uit te voeren, databases te beheren en gegevens te manipuleren.

## Gebruik
De basis syntaxis van de `mysql`-opdracht is als volgt:

```bash
mysql [options] [arguments]
```

## Veelvoorkomende opties
- `-u [username]`: Specificeert de gebruikersnaam voor de MySQL-database.
- `-p`: Vraagt om een wachtwoord voor de opgegeven gebruiker.
- `-h [hostname]`: Geeft de hostnaam van de MySQL-server op.
- `-D [database]`: Geeft de naam van de database op waarmee je wilt werken.
- `--execute="[query]"`: Voert een specifieke SQL-query uit en sluit daarna af.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `mysql`-opdracht:

1. Verbinden met een lokale MySQL-server:
   ```bash
   mysql -u root -p
   ```

2. Verbinden met een MySQL-server op een specifieke host:
   ```bash
   mysql -u user -p -h 192.168.1.100
   ```

3. Een specifieke database gebruiken:
   ```bash
   mysql -u user -p -D mydatabase
   ```

4. Een SQL-query uitvoeren vanuit de opdrachtregel:
   ```bash
   mysql -u user -p --execute="SELECT * FROM mytable;"
   ```

5. Een SQL-script uitvoeren:
   ```bash
   mysql -u user -p -D mydatabase < script.sql
   ```

## Tips
- Zorg ervoor dat je de juiste gebruikersrechten hebt voor de database waarmee je werkt.
- Gebruik de optie `--verbose` voor gedetailleerdere uitvoer van je commando's.
- Maak gebruik van SQL-scripts voor complexe query's om de leesbaarheid en herbruikbaarheid te verbeteren.
- Vergeet niet om je wachtwoord veilig te houden en niet in de opdrachtregel op te nemen om beveiligingsrisico's te vermijden.