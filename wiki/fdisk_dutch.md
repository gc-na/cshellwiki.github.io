# [Linux] Bash fdisk gebruik: Partities beheren op schijven

## Overview
De `fdisk`-opdracht is een krachtige tool voor het beheren van schijfpartities op Linux-systemen. Met `fdisk` kun je partities aanmaken, verwijderen en wijzigen op harde schijven en andere opslagapparaten.

## Usage
De basis syntaxis van de `fdisk`-opdracht is als volgt:

```bash
fdisk [opties] [apparaat]
```

Hierbij is `[apparaat]` meestal de schijf die je wilt beheren, zoals `/dev/sda`.

## Common Options
Hier zijn enkele veelvoorkomende opties voor `fdisk`:

- `-l`: Lijst alle beschikbare schijven en hun partities.
- `-u`: Gebruik sectoren in plaats van cylinders als eenheid.
- `-n`: Maak een nieuwe partitie aan.
- `-d`: Verwijder een bestaande partitie.
- `-p`: Toon de partitie-informatie van de opgegeven schijf.

## Common Examples
Hier zijn enkele praktische voorbeelden van het gebruik van `fdisk`:

1. **Lijst alle schijven en hun partities:**

   ```bash
   fdisk -l
   ```

2. **Een nieuwe partitie aanmaken:**

   ```bash
   fdisk /dev/sda
   ```

   Volg de prompts om een nieuwe partitie aan te maken.

3. **Een bestaande partitie verwijderen:**

   ```bash
   fdisk /dev/sda
   ```

   Selecteer de optie om een partitie te verwijderen en volg de instructies.

4. **De partitie-informatie van een specifieke schijf tonen:**

   ```bash
   fdisk -p /dev/sda
   ```

## Tips
- Zorg ervoor dat je een back-up maakt van belangrijke gegevens voordat je wijzigingen aanbrengt aan partities.
- Gebruik `fdisk` met voorzichtigheid, omdat onjuiste commando's kunnen leiden tot gegevensverlies.
- Raadpleeg de man-pagina (`man fdisk`) voor meer gedetailleerde informatie en opties.