# [Linux] Bash batch gebruik: Voer taken uit in de achtergrond

## Overzicht
De `batch` opdracht in Bash wordt gebruikt om taken in de achtergrond uit te voeren op een later tijdstip, wanneer het systeem minder druk is. Dit is handig voor het plannen van taken die veel systeembronnen vereisen, zonder dat je deze direct hoeft uit te voeren.

## Gebruik
De basis syntaxis van de `batch` opdracht is als volgt:

```bash
batch [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-l` : Specificeert dat de opdracht moet worden uitgevoerd met een bepaalde prioriteit.
- `-q` : Voert de opdracht uit in de achtergrond zonder output naar de terminal.
- `-h` : Toont de helpinformatie voor de `batch` opdracht.

## Veelvoorkomende Voorbeelden

1. **Een eenvoudige opdracht plannen**:
   Om een eenvoudige opdracht zoals `echo` in de achtergrond te plannen, gebruik je:
   ```bash
   echo "Hallo, wereld!" | batch
   ```

2. **Een script uitvoeren**:
   Je kunt ook een script plannen om later uit te voeren:
   ```bash
   /pad/naar/mijn_script.sh | batch
   ```

3. **Meerdere opdrachten plannen**:
   Je kunt meerdere opdrachten in één keer plannen door ze te scheiden met een puntkomma:
   ```bash
   (echo "Opdracht 1"; echo "Opdracht 2") | batch
   ```

## Tips
- Zorg ervoor dat je voldoende systeembronnen hebt voordat je zware taken plant.
- Controleer regelmatig de status van geplande taken met de `atq` opdracht.
- Gebruik `atrm` om ongewenste of foutieve taken te annuleren.

Met deze informatie kun je de `batch` opdracht effectief gebruiken om je taken efficiënt te plannen en uit te voeren.