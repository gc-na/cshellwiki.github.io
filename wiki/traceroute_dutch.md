# [Linux] Bash traceroute gebruik: Netwerkpaden traceren

## Overzicht
De `traceroute`-opdracht is een netwerkdiagnosetool die de route toont die gegevenspakketten nemen van de ene computer naar een andere op een netwerk. Het geeft inzicht in de verschillende knooppunten (routers) die de pakketten passeren, evenals de tijd die elk knooppunt nodig heeft om de gegevens te verwerken.

## Gebruik
De basis syntaxis van de `traceroute`-opdracht is als volgt:

```bash
traceroute [opties] [doel]
```

## Veelvoorkomende Opties
- `-m <max_hops>`: Stel het maximale aantal hops in dat traceroute mag volgen.
- `-w <timeout>`: Stel de tijdslimiet in voor het wachten op een antwoord van een hop.
- `-q <aantal>`: Bepaal het aantal echo-verzoeken dat naar elke hop wordt verzonden.
- `-n`: Voorkom DNS-resolutie en toon alleen IP-adressen.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `traceroute`:

1. Basis traceroute naar een website:
   ```bash
   traceroute www.example.com
   ```

2. Traceroute met een maximaal aantal hops van 15:
   ```bash
   traceroute -m 15 www.example.com
   ```

3. Traceroute met een tijdslimiet van 2 seconden:
   ```bash
   traceroute -w 2 www.example.com
   ```

4. Traceroute zonder DNS-resolutie:
   ```bash
   traceroute -n www.example.com
   ```

## Tips
- Gebruik de `-n` optie als je een snellere uitvoer wilt zonder te wachten op DNS-resolutie.
- Experimenteer met de `-q` optie om te zien hoeveel verzoeken je nodig hebt voor een betrouwbare meting.
- Controleer altijd de netwerkverbinding voordat je traceroute uitvoert om ervoor te zorgen dat je de juiste resultaten krijgt.