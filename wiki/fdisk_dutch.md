# [Linux] C Shell (csh) fdisk gebruik: Schijfpartities beheren

## Overzicht
Het `fdisk` commando wordt gebruikt om schijfpartities te beheren op Unix-achtige besturingssystemen. Het stelt gebruikers in staat om partities te maken, verwijderen en te wijzigen, wat essentieel is voor schijfbeheer.

## Gebruik
De basis syntaxis van het `fdisk` commando is als volgt:

```
fdisk [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-l`: Lijst alle beschikbare schijven en hun partities.
- `-u`: Gebruik sectoren als eenheid in plaats van cilinders.
- `-n`: Maak een nieuwe partitie aan.
- `-d`: Verwijder een bestaande partitie.
- `-p`: Toon de partitie-informatie van de geselecteerde schijf.

## Veelvoorkomende Voorbeelden
1. **Lijst beschikbare schijven en partities:**
   ```bash
   fdisk -l
   ```

2. **Een nieuwe partitie aanmaken:**
   ```bash
   fdisk /dev/sda
   ```
   Volg de instructies in de interactieve prompt om een nieuwe partitie te maken.

3. **Een bestaande partitie verwijderen:**
   ```bash
   fdisk /dev/sda
   ```
   Kies de optie om een partitie te verwijderen en volg de instructies.

4. **Partitie-informatie weergeven:**
   ```bash
   fdisk -p /dev/sda
   ```

## Tips
- Zorg ervoor dat je een back-up maakt van belangrijke gegevens voordat je wijzigingen aanbrengt aan partities.
- Gebruik `fdisk` met voorzichtigheid, vooral bij het verwijderen van partities, om gegevensverlies te voorkomen.
- Controleer altijd de huidige partitie-indeling met `fdisk -l` voordat je wijzigingen aanbrengt.