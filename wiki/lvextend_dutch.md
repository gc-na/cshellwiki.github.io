# [Linux] Bash lvextend gebruik: Vergroot logische volumes

## Overzicht
De `lvextend` opdracht wordt gebruikt om de grootte van een logisch volume in een Logical Volume Management (LVM) systeem te vergroten. Dit is nuttig wanneer je meer opslagruimte nodig hebt voor je bestanden of applicaties.

## Gebruik
De basis syntaxis van de `lvextend` opdracht is als volgt:

```bash
lvextend [opties] [argumenten]
```

## Veelvoorkomende opties
- `-L +<size>`: Voeg een specifieke grootte toe aan het volume.
- `-L <size>`: Stel de totale grootte van het volume in.
- `-r`: Vergroot het bestandssysteem automatisch na het vergroten van het volume.
- `-n`: Specificeer de naam van het logische volume dat je wilt vergroten.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `lvextend`:

1. **Voeg 10 GB toe aan een logisch volume**:
   ```bash
   lvextend -L +10G /dev/vgnaam/lvnaam
   ```

2. **Stel de totale grootte van een logisch volume in op 50 GB**:
   ```bash
   lvextend -L 50G /dev/vgnaam/lvnaam
   ```

3. **Vergroot het volume en het bestandssysteem automatisch**:
   ```bash
   lvextend -r -L +5G /dev/vgnaam/lvnaam
   ```

4. **Vergroot een logisch volume met een specifieke naam**:
   ```bash
   lvextend -n lvnaam /dev/vgnaam/lvnaam
   ```

## Tips
- Zorg ervoor dat je voldoende vrije ruimte hebt in de volume group voordat je een logisch volume vergroot.
- Gebruik de `-r` optie om het bestandssysteem automatisch uit te breiden, wat tijd en moeite bespaart.
- Controleer altijd de status van je logische volumes met `lvdisplay` na het uitvoeren van een uitbreiding om te bevestigen dat de wijzigingen correct zijn doorgevoerd.