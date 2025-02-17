# [Linux] Bash resize2fs gebruik: Schaal een bestandssysteem

## Overzicht
Het `resize2fs` commando wordt gebruikt om de grootte van een ext2, ext3 of ext4 bestandssysteem te wijzigen. Dit kan zowel het vergroten als het verkleinen van het bestandssysteem omvatten, afhankelijk van de beschikbare ruimte op de schijf.

## Gebruik
De basis syntaxis van het `resize2fs` commando is als volgt:

```bash
resize2fs [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-f`: Forceert de wijziging van de grootte, zelfs als het bestandssysteem niet gemonteerd is.
- `-p`: Toont voortgangsinformatie tijdens het schalen.
- `-s`: Schaal het bestandssysteem naar de opgegeven grootte.
- `-M`: Verklein het bestandssysteem tot de minimale grootte.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Vergroot een bestandssysteem
Om een ext4 bestandssysteem op `/dev/sda1` te vergroten, gebruik je:

```bash
resize2fs /dev/sda1
```

### Voorbeeld 2: Verklein een bestandssysteem
Om een ext4 bestandssysteem op `/dev/sda1` te verkleinen tot 10G, gebruik je:

```bash
resize2fs /dev/sda1 10G
```

### Voorbeeld 3: Voortgang tonen tijdens het schalen
Om de voortgang te tonen terwijl je een bestandssysteem vergroot, gebruik je:

```bash
resize2fs -p /dev/sda1
```

## Tips
- Zorg ervoor dat je een back-up maakt van belangrijke gegevens voordat je het bestandssysteem wijzigt.
- Het is aanbevolen om het bestandssysteem te ontkoppelen voordat je het verkleint om gegevensverlies te voorkomen.
- Controleer altijd de beschikbare ruimte met `df -h` voordat je een wijziging aanbrengt in de grootte van het bestandssysteem.