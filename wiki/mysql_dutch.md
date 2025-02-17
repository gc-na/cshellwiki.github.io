# [Linux] Bash mysql gebruik: Beheer en interactie met MySQL-databases

## Overzicht
De `mysql`-opdracht is een krachtige commandoregeltool die wordt gebruikt om te communiceren met MySQL-databases. Hiermee kunnen gebruikers SQL-query's uitvoeren, databases beheren en gegevens ophalen of bewerken.

## Gebruik
De basis syntaxis van de `mysql`-opdracht is als volgt:

```bash
mysql [options] [arguments]
```

## Veelvoorkomende opties
- `-u, --user=name`: Specificeert de gebruikersnaam voor de MySQL-verbinding.
- `-p, --password[=name]`: Vraagt om een wachtwoord voor de gebruiker. Als er geen wachtwoord wordt opgegeven, wordt om invoer gevraagd.
- `-h, --host=name`: Geeft de hostnaam van de MySQL-server op.
- `-D, --database=name`: Geeft de naam van de database op waarmee verbinding moet worden gemaakt.
- `--execute, -e`: Voert een opgegeven SQL-opdracht uit en sluit daarna de verbinding.

## Veelvoorkomende voorbeelden

### Verbinden met een lokale MySQL-server
```bash
mysql -u root -p
```

### Een specifieke database selecteren
```bash
mysql -u root -p -D mijn_database
```

### Een SQL-query uitvoeren vanuit de opdrachtregel
```bash
mysql -u root -p -e "SELECT * FROM gebruikers;"
```

### Een SQL-script uitvoeren
```bash
mysql -u root -p mijn_database < script.sql
```

### Lijst van databases opvragen
```bash
mysql -u root -p -e "SHOW DATABASES;"
```

## Tips
- Gebruik de optie `--verbose` om gedetailleerde uitvoer van de opdrachten te krijgen.
- Sla vaak gebruikte opdrachten op in een scriptbestand om ze eenvoudig opnieuw uit te voeren.
- Zorg ervoor dat je regelmatig back-ups maakt van je databases, vooral voordat je grote wijzigingen aanbrengt.