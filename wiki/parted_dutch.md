# [Linux] Bash parted gebruik: Partitiebeheer en schijfconfiguratie

## Overzicht
Het `parted` commando is een krachtige tool voor het beheren van schijfpartities in Linux. Het stelt gebruikers in staat om partities te maken, verwijderen, wijzigen en te controleren, waardoor het een essentieel hulpmiddel is voor systeembeheerders en gebruikers die hun schijfstructuur willen optimaliseren.

## Gebruik
De basis syntaxis van het `parted` commando is als volgt:

```bash
parted [opties] [argumenten]
```

## Veelvoorkomende opties
- `-l`, `--list`: Lijst alle beschikbare schijven en hun partities.
- `-s`, `--script`: Voert het commando uit zonder interactieve prompts.
- `mkpart`: Maakt een nieuwe partitie aan.
- `rm`: Verwijdert een bestaande partitie.
- `resizepart`: Wijzigt de grootte van een bestaande partitie.
- `print`: Toont de partitie-informatie van de geselecteerde schijf.

## Veelvoorkomende voorbeelden

### Lijst van schijven en partities
Om een lijst van alle schijven en hun partities weer te geven, gebruik je:

```bash
parted -l
```

### Een nieuwe partitie maken
Om een nieuwe partitie aan te maken op `/dev/sda`, gebruik je:

```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### Een partitie verwijderen
Om een partitie te verwijderen (bijvoorbeeld partitie 1 op `/dev/sda`), gebruik je:

```bash
parted /dev/sda rm 1
```

### De grootte van een partitie wijzigen
Om de grootte van een bestaande partitie aan te passen, gebruik je:

```bash
parted /dev/sda resizepart 1 200MiB
```

### Partitie-informatie weergeven
Om de details van de partities op een specifieke schijf te bekijken, gebruik je:

```bash
parted /dev/sda print
```

## Tips
- Zorg ervoor dat je een back-up maakt van belangrijke gegevens voordat je wijzigingen aanbrengt aan partities.
- Gebruik de `--script` optie om het proces te automatiseren zonder bevestigingen.
- Wees voorzichtig met het verwijderen of wijzigen van partities, aangezien dit gegevensverlies kan veroorzaken.