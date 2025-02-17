# [Linux] Bash yum gebruik: Beheer van softwarepakketten

## Overzicht
Het `yum`-commando (Yellowdog Updater, Modified) is een pakketbeheerder voor RPM-gebaseerde Linux-distributies. Het stelt gebruikers in staat om softwarepakketten te installeren, bij te werken en te verwijderen, evenals om afhankelijkheden automatisch te beheren.

## Gebruik
De basis syntaxis van het `yum`-commando is als volgt:

```bash
yum [opties] [argumenten]
```

## Veelvoorkomende opties
- `install`: Installeert een of meerdere pakketten.
- `remove`: Verwijdert een of meerdere pakketten.
- `update`: Werkt geïnstalleerde pakketten bij naar de nieuwste versie.
- `list`: Toont een lijst van beschikbare of geïnstalleerde pakketten.
- `search`: Zoekt naar pakketten op basis van een zoekterm.
- `info`: Toont informatie over een specifiek pakket.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `yum`:

- **Een pakket installeren:**
  ```bash
  yum install pakketnaam
  ```

- **Een pakket verwijderen:**
  ```bash
  yum remove pakketnaam
  ```

- **Alle geïnstalleerde pakketten bijwerken:**
  ```bash
  yum update
  ```

- **Een lijst van beschikbare pakketten tonen:**
  ```bash
  yum list available
  ```

- **Zoeken naar een specifiek pakket:**
  ```bash
  yum search zoekterm
  ```

- **Informatie over een pakket opvragen:**
  ```bash
  yum info pakketnaam
  ```

## Tips
- Zorg ervoor dat je `yum` uitvoert met root-rechten om toegang te krijgen tot alle functies.
- Gebruik `yum clean all` om de cache van `yum` op te schonen en schijfruimte vrij te maken.
- Controleer regelmatig op updates om je systeem veilig en up-to-date te houden.
- Maak gebruik van de `--assumeyes` optie om bevestigingen automatisch te accepteren tijdens installaties of updates.