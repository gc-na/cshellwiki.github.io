# [Linux] Bash lvcreate gebruik: Maak logische volumes aan

## Overzicht
De `lvcreate` opdracht wordt gebruikt om nieuwe logische volumes aan te maken binnen een Logical Volume Manager (LVM) configuratie. Dit stelt gebruikers in staat om flexibele opslagoplossingen te creëren door schijfruimte te beheren en toe te wijzen aan verschillende volumes.

## Gebruik
De basis syntaxis van de `lvcreate` opdracht is als volgt:

```bash
lvcreate [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n, --name <naam>`: Specificeert de naam van het nieuwe logische volume.
- `-L, --size <grootte>`: Bepaalt de grootte van het logische volume.
- `-l, --extents <aantal>`: Geeft het aantal extents aan dat moet worden toegewezen aan het volume.
- `-C, --mirrors <aantal>`: Maakt een aantal spiegelkopieën van het volume aan.
- `-Z, --zeroing` : Zeroes the volume before creating it (standaard is dit aan).

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Een eenvoudig logische volume aanmaken
```bash
lvcreate -n mijn_volume -L 10G mijn_vg
```
Dit commando maakt een logische volume genaamd `mijn_volume` aan met een grootte van 10 GB in de volume groep `mijn_vg`.

### Voorbeeld 2: Een logische volume met extents aanmaken
```bash
lvcreate -n mijn_extents_volume -l 100 mijn_vg
```
Hiermee wordt een logische volume aangemaakt met 100 extents in de volume groep `mijn_vg`.

### Voorbeeld 3: Een spiegelvolume aanmaken
```bash
lvcreate -n mijn_spiegel_volume -L 20G -m 1 mijn_vg
```
Dit commando maakt een spiegelvolume aan met de naam `mijn_spiegel_volume` van 20 GB in de volume groep `mijn_vg`.

## Tips
- Zorg ervoor dat je voldoende vrije ruimte in je volume groep hebt voordat je een nieuw logische volume aanmaakt.
- Gebruik duidelijke en beschrijvende namen voor je logische volumes om verwarring te voorkomen.
- Overweeg het gebruik van spiegelingen voor belangrijke volumes om dataverlies te minimaliseren.