# [Linux] Bash mpstat gebruik: Toont CPU-statistieken

## Overzicht
De `mpstat`-opdracht is een onderdeel van de sysstat-toolset en wordt gebruikt om CPU-statistieken te verzamelen en weer te geven. Het biedt informatie over de CPU-belasting, inclusief het percentage tijd dat de CPU actief is, inactief is of wacht op I/O-bewerkingen. Dit is nuttig voor systeembeheerders om de prestaties van hun systemen te monitoren.

## Gebruik
De basis syntaxis van de `mpstat`-opdracht is als volgt:

```bash
mpstat [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-P ALL`: Toon statistieken voor alle CPU's.
- `-u`: Toon de CPU-gebruikstatistieken.
- `-h`: Toon een helpbericht met beschikbare opties.
- `interval`: Geef het interval in seconden op voor het verzamelen van gegevens.
- `count`: Geef het aantal keren op dat de statistieken moeten worden weergegeven.

## Veelvoorkomende Voorbeelden

1. Toon CPU-statistieken voor alle CPU's:
   ```bash
   mpstat -P ALL
   ```

2. Toon CPU-gebruikstatistieken elke 2 seconden, 5 keer:
   ```bash
   mpstat -u 2 5
   ```

3. Toon alleen de statistieken voor de eerste CPU:
   ```bash
   mpstat -P 0
   ```

4. Toon een helpbericht met beschikbare opties:
   ```bash
   mpstat -h
   ```

## Tips
- Gebruik `mpstat` in combinatie met andere monitoringtools zoals `top` of `htop` voor een uitgebreidere analyse van systeembronnen.
- Monitor regelmatig de CPU-statistieken om trends in gebruik te identificeren en om mogelijke prestatieproblemen vroegtijdig op te sporen.
- Experimenteer met verschillende intervallen en tellingen om een beter inzicht te krijgen in de CPU-prestaties tijdens piekuren.