# [Linux] Bash mtr gebruik: Netwerkdiagnose en traceroute

## Overzicht
De `mtr` (My Traceroute) opdracht combineert de functionaliteit van `ping` en `traceroute` om netwerkverbindingen te analyseren. Het biedt real-time informatie over de route die pakketten afleggen naar een doelhost en meet de latentie en pakketverlies op elke hop.

## Gebruik
De basis syntaxis van de `mtr` opdracht is als volgt:

```bash
mtr [opties] [doel]
```

## Veelvoorkomende Opties
- `-r`: Voer een rapportmodus uit, wat betekent dat de resultaten alleen aan het einde worden weergegeven.
- `-c [aantal]`: Specificeer het aantal pings dat moet worden verzonden.
- `-i [interval]`: Stel het interval in tussen pings in seconden.
- `-p`: Voer de opdracht uit in de poortmodus, wat nuttig is voor het testen van specifieke poorten.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `mtr`:

1. Basis gebruik om de route naar een host te traceren:
   ```bash
   mtr example.com
   ```

2. Rapportmodus gebruiken om een samenvatting van de resultaten te krijgen:
   ```bash
   mtr -r example.com
   ```

3. Aantal pings instellen op 10:
   ```bash
   mtr -c 10 example.com
   ```

4. Een interval van 2 seconden tussen pings instellen:
   ```bash
   mtr -i 2 example.com
   ```

5. Traceroute uitvoeren naar een specifieke poort:
   ```bash
   mtr -p -c 5 -r example.com 80
   ```

## Tips
- Gebruik de rapportmodus (`-r`) voor een overzichtelijke weergave van de resultaten, vooral als je een groot aantal pings uitvoert.
- Experimenteer met verschillende intervallen om te zien hoe de netwerkprestaties variëren.
- Combineer `mtr` met andere netwerktools zoals `ping` en `traceroute` voor een uitgebreidere diagnose van netwerkproblemen.