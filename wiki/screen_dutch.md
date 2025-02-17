# [Linux] Bash screen gebruik: Beheer meerdere terminalsessies

## Overzicht
De `screen`-opdracht is een terminalmultiplexer die gebruikers in staat stelt om meerdere terminalsessies binnen één enkele terminalvenster te beheren. Het biedt de mogelijkheid om sessies te detacheren en later weer aan te sluiten, wat handig is voor langdurige processen of wanneer je je verbinding verliest.

## Gebruik
De basis syntaxis van de `screen`-opdracht is als volgt:

```
screen [opties] [argumenten]
```

## Veelvoorkomende opties
- `-S <naam>`: Geef een naam aan de nieuwe sessie.
- `-d -r`: Detacheren van een sessie en deze opnieuw verbinden.
- `-list`: Lijst alle actieve screen-sessies.
- `-h <lijnen>`: Stel het aantal regels in dat wordt opgeslagen in de scrollbuffer.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `screen`-opdracht:

### Een nieuwe screen-sessie starten
```bash
screen
```

### Een nieuwe sessie met een specifieke naam starten
```bash
screen -S mijn_sessie
```

### Een detach-sessie opnieuw verbinden
```bash
screen -d -r mijn_sessie
```

### Lijst van actieve screen-sessies weergeven
```bash
screen -list
```

### Scrollbuffer instellen op 1000 lijnen
```bash
screen -h 1000
```

## Tips
- Gebruik een herkenbare naam voor je sessies met de `-S` optie, zodat je ze gemakkelijk kunt terugvinden.
- Vergeet niet om je sessies te detacheren met `Ctrl+A` gevolgd door `D` als je tijdelijk wilt weggaan.
- Maak gebruik van de scrollfunctie in screen door `Ctrl+A` gevolgd door `[` te gebruiken om door de output te scrollen.