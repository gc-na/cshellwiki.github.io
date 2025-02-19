# [Linux] C Shell (csh) udevadm gebruik: Beheer van udev apparaten

## Overzicht
Het `udevadm` commando is een hulpmiddel voor het beheren van de udev daemon, die verantwoordelijk is voor het dynamisch beheren van apparaten in Linux-systemen. Met `udevadm` kunnen gebruikers informatie over apparaten opvragen, regels beheren en de status van de udev daemon controleren.

## Gebruik
De basis syntaxis van het `udevadm` commando is als volgt:

```
udevadm [opties] [argumenten]
```

## Veelvoorkomende opties
- `info`: Toont informatie over een specifiek apparaat.
- `trigger`: Activeert de udev regels voor alle apparaten of een specifiek apparaat.
- `control`: Beheert de udev daemon, zoals het herladen van regels.
- `settle`: Wacht tot alle udev gebeurtenissen zijn afgehandeld.

## Veelvoorkomende voorbeelden

### Apparatinformatie opvragen
Om informatie over een specifiek apparaat op te vragen, gebruik je het `info` commando:

```csh
udevadm info --query=all --name=/dev/sda
```

### Apparaten triggeren
Om de udev regels voor een specifiek apparaat te activeren, gebruik je het `trigger` commando:

```csh
udevadm trigger --subsystem=net
```

### Udev daemon herladen
Als je wijzigingen hebt aangebracht in de udev regels, kun je de daemon herladen met:

```csh
udevadm control --reload-rules
```

### Wachten op udev gebeurtenissen
Om te wachten tot alle udev gebeurtenissen zijn afgehandeld, gebruik je:

```csh
udevadm settle
```

## Tips
- Zorg ervoor dat je de juiste rechten hebt om `udevadm` commando's uit te voeren, vaak zijn root-rechten vereist.
- Gebruik `udevadm monitor` om live udev gebeurtenissen te volgen, wat handig kan zijn voor het debuggen.
- Controleer regelmatig de udev regels in `/etc/udev/rules.d/` om ervoor te zorgen dat je systeem goed geconfigureerd is.