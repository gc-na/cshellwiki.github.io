# [Linux] C Shell (csh) parted gebruik: Schijfpartitionering en -beheer

## Overzicht
Het `parted` commando is een krachtige tool voor het beheren van schijfpartities. Het stelt gebruikers in staat om partities te maken, te verwijderen, te verkleinen en te vergroten, evenals andere bewerkingen uit te voeren op schijven en partities.

## Gebruik
De basis syntaxis van het `parted` commando is als volgt:

```csh
parted [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-l`: Lijst alle beschikbare schijven en hun partities.
- `mkpart`: Maakt een nieuwe partitie aan.
- `rm`: Verwijdert een bestaande partitie.
- `resizepart`: Wijzigt de grootte van een bestaande partitie.
- `print`: Toont de huidige partitie-informatie van de geselecteerde schijf.

## Veelvoorkomende Voorbeelden

### Lijst van schijven en partities
```csh
parted -l
```

### Een nieuwe partitie maken
```csh
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### Een partitie verwijderen
```csh
parted /dev/sda rm 1
```

### De grootte van een partitie wijzigen
```csh
parted /dev/sda resizepart 1 200MiB
```

### Huidige partitie-informatie weergeven
```csh
parted /dev/sda print
```

## Tips
- Zorg ervoor dat je een back-up maakt van belangrijke gegevens voordat je wijzigingen aanbrengt aan partities.
- Gebruik `parted` met voorzichtigheid, vooral bij het verwijderen of wijzigen van partities, omdat dit gegevensverlies kan veroorzaken.
- Controleer altijd de huidige partitie-informatie met de `print` optie voordat je wijzigingen aanbrengt.