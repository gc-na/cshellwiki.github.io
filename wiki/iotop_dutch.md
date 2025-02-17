# [Linux] Bash iotop gebruik: Monitoren van schijfactiviteit in realtime

## Overzicht
Het `iotop` commando is een nuttig hulpmiddel voor het monitoren van schijfactiviteit in realtime. Het toont welke processen de meeste I/O-bronnen gebruiken, waardoor je beter inzicht krijgt in de prestaties van je systeem.

## Gebruik
De basis syntaxis van het `iotop` commando is als volgt:

```bash
iotop [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-o`, `--only`: Toont alleen processen die momenteel I/O-activiteit genereren.
- `-b`, `--batch`: Voert `iotop` uit in batchmodus, wat handig is voor logging.
- `-n NUM`, `--iter=NUM`: Aantal iteraties dat `iotop` moet uitvoeren voordat het stopt.
- `-d SEC`, `--delay=SEC`: Stel de vertraging in tussen updates in seconden.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `iotop`:

1. **Basis gebruik van iotop**:
   ```bash
   iotop
   ```

2. **Alleen processen met I/O-activiteit tonen**:
   ```bash
   iotop -o
   ```

3. **Uitvoeren in batchmodus voor logging**:
   ```bash
   iotop -b -n 5
   ```

4. **Vertraging instellen tussen updates**:
   ```bash
   iotop -d 2
   ```

## Tips
- Gebruik `iotop` met rootrechten voor volledige toegang tot alle processen.
- Combineer `iotop` met andere monitoringtools zoals `htop` voor een completer overzicht van systeembronnen.
- Let op processen die constant hoge I/O-activiteit vertonen; dit kan wijzen op inefficiënte toepassingen of problemen met de schijf.