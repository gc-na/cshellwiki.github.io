# [Linux] C Shell (csh) vmstat gebruik: systeemstatusmonitoring

## Overzicht
De `vmstat` (virtual memory statistics) opdracht geeft informatie weer over de systeemstatus, inclusief geheugen, processen, en CPU-activiteit. Het is een nuttig hulpmiddel voor systeembeheerders om de prestaties van een systeem te analyseren.

## Gebruik
De basis syntaxis van de `vmstat` opdracht is als volgt:

```csh
vmstat [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-s`: Toon een samenvatting van systeemstatistieken.
- `-m`: Toon informatie over geheugenpagina's.
- `-d`: Toon schijfstatistieken.
- `interval`: Geef een tijdsinterval in seconden om de statistieken periodiek te vernieuwen.
- `count`: Geef het aantal keren aan dat de statistieken moeten worden weergegeven.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `vmstat`:

1. **Basis systeemstatistieken weergeven:**
   ```csh
   vmstat
   ```

2. **Statistieken elke 5 seconden vernieuwen:**
   ```csh
   vmstat 5
   ```

3. **Toon een samenvatting van systeemstatistieken:**
   ```csh
   vmstat -s
   ```

4. **Toon schijfstatistieken:**
   ```csh
   vmstat -d
   ```

5. **Statistieken elke 2 seconden voor 10 keer weergeven:**
   ```csh
   vmstat 2 10
   ```

## Tips
- Gebruik `vmstat` samen met andere monitoringtools voor een completer beeld van de systeemprestaties.
- Let op de kolommen voor geheugen- en CPU-gebruik om knelpunten in de prestaties te identificeren.
- Experimenteer met verschillende intervallen en tellingen om de meest relevante gegevens voor jouw situatie te verkrijgen.