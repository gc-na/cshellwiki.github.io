# [Linux] Bash vgcreate gebruik: Maak een nieuwe volume group aan

## Overzicht
De `vgcreate` opdracht in Bash wordt gebruikt om een nieuwe volume group (VG) aan te maken in een Logical Volume Management (LVM) systeem. Dit stelt gebruikers in staat om schijfruimte te beheren en te organiseren in logische volumes.

## Gebruik
De basis syntaxis van de `vgcreate` opdracht is als volgt:

```bash
vgcreate [opties] [naam_vg] [fysieke_volumes]
```

## Veelvoorkomende Opties
- `-s, --stripes <n>`: Specificeert het aantal stripes voor de volume group.
- `-p, --maxlogicalvolumes <n>`: Bepaalt het maximale aantal logische volumes dat in de volume group kan worden aangemaakt.
- `-n, --noudevsync`: Voorkomt dat de udev daemon wordt gesynchroniseerd met de nieuwe volume group.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Een eenvoudige volume group aanmaken
```bash
vgcreate mijn_vg /dev/sda1 /dev/sda2
```
Dit creëert een nieuwe volume group genaamd `mijn_vg` met de fysieke volumes `/dev/sda1` en `/dev/sda2`.

### Voorbeeld 2: Een volume group aanmaken met specifieke stripes
```bash
vgcreate -s 64k mijn_vg /dev/sdb1
```
Hiermee wordt een volume group `mijn_vg` aangemaakt met een stripe-grootte van 64 kilobytes op het fysieke volume `/dev/sdb1`.

### Voorbeeld 3: Een volume group aanmaken zonder udev-synchronisatie
```bash
vgcreate -n mijn_vg /dev/sdc1
```
Dit creëert de volume group `mijn_vg` zonder de udev daemon te synchroniseren.

## Tips
- Zorg ervoor dat de fysieke volumes die je gebruikt voor `vgcreate` niet in gebruik zijn door andere systemen of processen.
- Controleer altijd de beschikbare schijfruimte voordat je een nieuwe volume group aanmaakt om ervoor te zorgen dat je voldoende ruimte hebt.
- Gebruik de `vgdisplay` opdracht om de details van je volume groups te bekijken na het aanmaken.