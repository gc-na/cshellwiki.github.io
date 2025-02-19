# [Linux] C Shell (csh) traceroute6 gebruik: Netwerkpaden traceren

## Overzicht
De `traceroute6` opdracht wordt gebruikt om het pad te traceren dat IPv6-pakketten volgen van de lokale machine naar een opgegeven bestemming. Dit helpt bij het identificeren van netwerkproblemen door de tussenliggende routers en hun reactietijden te tonen.

## Gebruik
De basis syntaxis van de `traceroute6` opdracht is als volgt:

```csh
traceroute6 [opties] [doel]
```

## Veelvoorkomende Opties
- `-n`: Toon IP-adressen in plaats van hostnamen.
- `-m max_ttl`: Stel de maximale Time-To-Live (TTL) in voor de traceroute.
- `-p port`: Specificeer de poort die gebruikt moet worden voor de traceroute.
- `-q nqueries`: Geef het aantal echo-verzoeken op dat per hop moet worden verzonden.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `traceroute6`:

1. Basis traceroute naar een IPv6-adres:
   ```csh
   traceroute6 2001:db8::1
   ```

2. Traceroute met het tonen van IP-adressen in plaats van hostnamen:
   ```csh
   traceroute6 -n 2001:db8::1
   ```

3. Traceroute met een maximale TTL van 30:
   ```csh
   traceroute6 -m 30 2001:db8::1
   ```

4. Traceroute naar een specifieke poort:
   ```csh
   traceroute6 -p 80 2001:db8::1
   ```

5. Traceroute met meerdere echo-verzoeken per hop:
   ```csh
   traceroute6 -q 5 2001:db8::1
   ```

## Tips
- Gebruik de `-n` optie om de snelheid van de traceroute te verhogen, vooral als DNS-resolutie traag is.
- Controleer de configuratie van je firewall, aangezien deze de traceroute-uitvoer kan beïnvloeden.
- Combineer `traceroute6` met andere netwerkdiagnosetools zoals `ping` voor een completer beeld van netwerkprestaties.