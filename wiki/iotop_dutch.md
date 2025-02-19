# [Linux] C Shell (csh) iotop gebruik: Monitoren van schijfactiviteit

## Overzicht
De `iotop` opdracht is een nuttig hulpmiddel voor het monitoren van schijfactiviteit in een Linux-omgeving. Het toont welke processen de meeste I/O-bronnen gebruiken, waardoor je inzicht krijgt in de prestaties van je systeem.

## Gebruik
De basis syntaxis van de `iotop` opdracht is als volgt:

```bash
iotop [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-o` : Toon alleen processen die momenteel I/O-activiteit genereren.
- `-b` : Voer `iotop` uit in batchmodus, wat handig is voor logging.
- `-n NUM` : Geef het aantal iteraties op voordat `iotop` stopt (alleen in batchmodus).
- `-d SECONDS` : Stel de vertraging in tussen updates in batchmodus.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `iotop`:

1. **Basis gebruik van iotop**:
   ```bash
   iotop
   ```

2. **Alleen processen met I/O-activiteit weergeven**:
   ```bash
   iotop -o
   ```

3. **Uitvoeren in batchmodus met 5 seconden vertraging**:
   ```bash
   iotop -b -d 5
   ```

4. **Batchmodus met 10 iteraties**:
   ```bash
   iotop -b -n 10
   ```

## Tips
- Gebruik `iotop` met rootrechten voor volledige toegang tot alle processen.
- Combineer `iotop` met andere monitoringtools zoals `htop` voor een uitgebreider overzicht van systeembronnen.
- Regelmatig gebruik van `iotop` kan helpen bij het identificeren van processen die de systeemprestaties negatief beïnvloeden.