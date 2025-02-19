# [Linux] C Shell (csh) tune2fs gebruik: Wijzig bestandssysteemparameters

## Overzicht
De `tune2fs` opdracht wordt gebruikt om de parameters van een ext2, ext3 of ext4 bestandssysteem aan te passen. Hiermee kunnen gebruikers instellingen zoals de maximale aantal mounts, journal-instellingen en andere belangrijke parameters configureren.

## Gebruik
De basis syntaxis van de `tune2fs` opdracht is als volgt:

```csh
tune2fs [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c <aantal>`: Stel het maximale aantal mounts in voordat het bestandssysteem moet worden gecontroleerd.
- `-i <interval>`: Stel de tijdsperiode in tussen controles van het bestandssysteem.
- `-j`: Zet het journal aan voor een ext2 bestandssysteem.
- `-O <opties>`: Voeg specifieke opties toe aan het bestandssysteem.
- `-L <label>`: Wijzig het label van het bestandssysteem.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `tune2fs`:

1. Stel het maximale aantal mounts in op 20:
   ```csh
   tune2fs -c 20 /dev/sda1
   ```

2. Stel de tijdsperiode tussen controles in op 30 dagen:
   ```csh
   tune2fs -i 30d /dev/sda1
   ```

3. Zet het journal aan voor een ext2 bestandssysteem:
   ```csh
   tune2fs -j /dev/sda1
   ```

4. Wijzig het label van het bestandssysteem naar "Data":
   ```csh
   tune2fs -L Data /dev/sda1
   ```

## Tips
- Zorg ervoor dat je een back-up maakt van belangrijke gegevens voordat je wijzigingen aanbrengt in het bestandssysteem.
- Controleer altijd de huidige instellingen met `tune2fs -l /dev/sda1` voordat je wijzigingen aanbrengt.
- Gebruik `man tune2fs` voor meer gedetailleerde informatie over de beschikbare opties en hun gebruik.