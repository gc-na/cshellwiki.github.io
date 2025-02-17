# [Linux] Bash dpkg gebruik: Beheer van Debian-pakketten

## Overzicht
De `dpkg`-opdracht is een laag-niveau pakketbeheerder voor Debian-gebaseerde systemen. Het wordt gebruikt om softwarepakketten te installeren, te verwijderen en te beheren op een systeem dat het Debian-pakketformaat gebruikt.

## Gebruik
De basis syntaxis van de `dpkg`-opdracht is als volgt:

```bash
dpkg [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-i`, `--install`: Installeert een pakket.
- `-r`, `--remove`: Verwijdert een geïnstalleerd pakket.
- `-l`, `--list`: Lijst alle geïnstalleerde pakketten op.
- `-s`, `--status`: Toont de status van een specifiek pakket.
- `-P`, `--purge`: Verwijdert een pakket en zijn configuratiebestanden.

## Veelvoorkomende Voorbeelden
- **Een pakket installeren:**
  ```bash
  sudo dpkg -i pakketnaam.deb
  ```

- **Een pakket verwijderen:**
  ```bash
  sudo dpkg -r pakketnaam
  ```

- **Een pakket en zijn configuratiebestanden verwijderen:**
  ```bash
  sudo dpkg -P pakketnaam
  ```

- **Lijst van alle geïnstalleerde pakketten:**
  ```bash
  dpkg -l
  ```

- **Status van een specifiek pakket controleren:**
  ```bash
  dpkg -s pakketnaam
  ```

## Tips
- Gebruik `dpkg` in combinatie met `apt` voor een betere gebruikerservaring, aangezien `apt` automatisch afhankelijkheden beheert.
- Controleer altijd de status van een pakket na installatie of verwijdering om te bevestigen dat de actie succesvol was.
- Maak gebruik van de `--help` optie om meer informatie over de beschikbare opties te krijgen:
  ```bash
  dpkg --help
  ```