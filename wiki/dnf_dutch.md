# [Linux] Bash dnf gebruik: Beheer van softwarepakketten

## Overzicht
De `dnf` (Dandified YUM) command is een pakketbeheerder voor RPM-gebaseerde Linux-distributies, zoals Fedora en CentOS. Het stelt gebruikers in staat om softwarepakketten te installeren, bij te werken en te verwijderen, evenals om afhankelijkheden te beheren.

## Gebruik
De basis syntaxis van de `dnf` command is als volgt:

```bash
dnf [opties] [argumenten]
```

## Veelvoorkomende Opties
- `install`: Installeert een of meer pakketten.
- `remove`: Verwijdert een of meer pakketten.
- `update`: Werkt geïnstalleerde pakketten bij naar de nieuwste versie.
- `search`: Zoekt naar pakketten op basis van naam of beschrijving.
- `info`: Toont informatie over een specifiek pakket.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `dnf` command:

### Een pakket installeren
```bash
dnf install pakketnaam
```

### Een pakket verwijderen
```bash
dnf remove pakketnaam
```

### Alle geïnstalleerde pakketten bijwerken
```bash
dnf update
```

### Zoeken naar een pakket
```bash
dnf search zoekterm
```

### Informatie over een specifiek pakket opvragen
```bash
dnf info pakketnaam
```

## Tips
- Gebruik `dnf clean all` om de cache op te schonen en schijfruimte vrij te maken.
- Controleer regelmatig op updates met `dnf update` om je systeem veilig en up-to-date te houden.
- Combineer opties, zoals `dnf install --assumeyes pakketnaam`, om bevestigingen automatisch te accepteren tijdens de installatie.