# [Linux] Bash pkg gebruik: Beheer van softwarepakketten

## Overzicht
De `pkg`-opdracht is een hulpmiddel voor het beheren van softwarepakketten op systemen die gebruikmaken van het FreeBSD-pakketbeheersysteem. Het stelt gebruikers in staat om pakketten te installeren, bij te werken en te verwijderen, evenals om informatie over geïnstalleerde pakketten op te vragen.

## Gebruik
De basis syntaxis van de `pkg`-opdracht is als volgt:

```bash
pkg [opties] [argumenten]
```

## Veelvoorkomende Opties
- `install`: Installeert een of meerdere pakketten.
- `remove`: Verwijdert een of meerdere pakketten.
- `update`: Werkt de lijst met beschikbare pakketten bij.
- `upgrade`: Werkt geïnstalleerde pakketten bij naar de nieuwste versies.
- `info`: Toont informatie over een specifiek pakket.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `pkg`-opdracht:

### Een pakket installeren
```bash
pkg install vim
```

### Een pakket verwijderen
```bash
pkg remove vim
```

### De lijst met beschikbare pakketten bijwerken
```bash
pkg update
```

### Geïnstalleerde pakketten bijwerken
```bash
pkg upgrade
```

### Informatie over een specifiek pakket opvragen
```bash
pkg info vim
```

## Tips
- Zorg ervoor dat je regelmatig `pkg update` uitvoert om de lijst met beschikbare pakketten up-to-date te houden.
- Gebruik `pkg search <pakketnaam>` om naar specifieke pakketten te zoeken.
- Controleer de afhankelijkheden van een pakket met de optie `-d` bij de `pkg info` opdracht om te zien welke andere pakketten nodig zijn.