# [Linux] C Shell (csh) vgextend gebruik: Voeg fysieke volumes toe aan een volume group

## Overzicht
De `vgextend` opdracht wordt gebruikt om fysieke volumes toe te voegen aan een bestaande volume group in een Logical Volume Manager (LVM) configuratie. Dit stelt gebruikers in staat om de opslagcapaciteit van een volume group uit te breiden door extra schijven of partities toe te voegen.

## Gebruik
De basis syntaxis van de `vgextend` opdracht is als volgt:

```
vgextend [opties] [volume_group] [fysieke_volumes]
```

## Veelvoorkomende Opties
- `-f`: Forceert de uitbreiding, zelfs als sommige fysieke volumes niet beschikbaar zijn.
- `-n`: Negeert de foutmeldingen en gaat door met de uitbreiding.
- `--test`: Voert een test uit zonder daadwerkelijk wijzigingen aan te brengen.

## Veelvoorkomende Voorbeelden

1. **Voeg een fysiek volume toe aan een volume group:**
   ```csh
   vgextend my_volume_group /dev/sdb1
   ```

2. **Voeg meerdere fysieke volumes toe:**
   ```csh
   vgextend my_volume_group /dev/sdb1 /dev/sdc1
   ```

3. **Forceer de uitbreiding van een volume group:**
   ```csh
   vgextend -f my_volume_group /dev/sdb1
   ```

4. **Voer een test uit zonder wijzigingen aan te brengen:**
   ```csh
   vgextend --test my_volume_group /dev/sdb1
   ```

## Tips
- Zorg ervoor dat de fysieke volumes die je wilt toevoegen geconfigureerd zijn als LVM voordat je `vgextend` gebruikt.
- Controleer altijd de status van je volume group na het uitvoeren van de `vgextend` opdracht met `vgdisplay`.
- Gebruik de `--test` optie om te verifiëren dat de uitbreiding succesvol zal zijn zonder daadwerkelijk wijzigingen aan te brengen.