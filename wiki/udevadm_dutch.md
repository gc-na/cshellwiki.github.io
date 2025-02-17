# [Linux] Bash udevadm gebruik: Beheer van apparaatbeheer

## Overzicht
Het `udevadm` commando is een hulpmiddel voor het beheren van de udev daemon, die verantwoordelijk is voor het dynamisch beheren van apparaatbestanden in Linux. Het stelt gebruikers in staat om informatie over apparaten te bekijken, regels te beheren en de status van de udev daemon te controleren.

## Gebruik
De basisstructuur van het `udevadm` commando is als volgt:

```bash
udevadm [opties] [argumenten]
```

## Veelvoorkomende Opties
- `info`: Toon informatie over een specifiek apparaat.
- `trigger`: Activeer de regels voor een specifiek apparaat of alle apparaten.
- `settle`: Wacht tot alle udev gebeurtenissen zijn afgehandeld.
- `control`: Beheer de udev daemon, zoals het herstarten of stoppen ervan.

## Veelvoorkomende Voorbeelden

### Apparaatinformatie opvragen
Om informatie over een specifiek apparaat op te vragen, gebruik je het `info` commando:

```bash
udevadm info --query=all --name=/dev/sda
```

### Apparaten triggeren
Om de udev regels voor een bepaald apparaat te activeren, gebruik je het `trigger` commando:

```bash
udevadm trigger --subsystem=block
```

### Wachten op udev gebeurtenissen
Als je wilt wachten tot alle udev gebeurtenissen zijn afgehandeld, gebruik je:

```bash
udevadm settle
```

### Udev daemon beheren
Om de udev daemon opnieuw te starten, gebruik je:

```bash
udevadm control --reload-rules
```

## Tips
- Gebruik `udevadm info` om snel te controleren welke regels van toepassing zijn op een apparaat.
- Wees voorzichtig met het `trigger` commando, omdat dit kan leiden tot onbedoelde acties op apparaten.
- Regelmatig de udev regels herladen kan helpen bij het oplossen van problemen met apparaatdetectie.