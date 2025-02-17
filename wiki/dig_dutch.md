# [Linux] Bash dig gebruik: DNS-query's uitvoeren

## Overzicht
De `dig` (Domain Information Groper) opdracht is een krachtige tool die wordt gebruikt om DNS-informatie op te vragen. Het stelt gebruikers in staat om gedetailleerde informatie over domeinnamen en hun bijbehorende IP-adressen te verkrijgen, wat nuttig is voor netwerkbeheer en probleemoplossing.

## Gebruik
De basis syntaxis van de `dig` opdracht is als volgt:

```bash
dig [opties] [argumenten]
```

## Veelvoorkomende Opties
- `@server`: Specificeert de DNS-server die moet worden geraadpleegd.
- `-t type`: Bepaalt het type DNS-record dat moet worden opgevraagd (bijv. A, MX, TXT).
- `+short`: Geeft een verkorte uitvoer van het resultaat.
- `+trace`: Volgt de resolutie van het domein stap voor stap.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `dig` opdracht:

### Basis A-record opvragen
Om het A-record van een domein op te vragen, gebruik je:

```bash
dig example.com
```

### Specifiek type record opvragen
Om het MX-record van een domein op te vragen, gebruik je:

```bash
dig -t MX example.com
```

### Gebruik maken van een specifieke DNS-server
Om een DNS-query uit te voeren via een specifieke server, bijvoorbeeld Google DNS:

```bash
dig @8.8.8.8 example.com
```

### Verkorte uitvoer
Voor een beknoptere uitvoer van het A-record:

```bash
dig +short example.com
```

### Trace van de resolutie
Om de volledige resolutie van een domein te volgen:

```bash
dig +trace example.com
```

## Tips
- Gebruik de `+short` optie voor een snellere en eenvoudigere uitvoer, vooral als je alleen het IP-adres nodig hebt.
- Combineer `dig` met andere commando's zoals `grep` om specifieke informatie uit de uitvoer te filteren.
- Vergeet niet dat de resultaten van `dig` kunnen variëren afhankelijk van de DNS-server die je gebruikt.