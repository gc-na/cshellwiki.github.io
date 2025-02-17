# [Linux] Bash traceroute6 gebruik: Netwerkpaden traceren met IPv6

## Overzicht
De `traceroute6` opdracht wordt gebruikt om het pad te traceren dat IPv6-pakketten nemen van de lokale machine naar een opgegeven bestemming. Het geeft inzicht in de verschillende routers die de gegevens onderweg passeren en helpt bij het diagnosticeren van netwerkproblemen.

## Gebruik
De basis syntaxis van de `traceroute6` opdracht is als volgt:

```bash
traceroute6 [opties] [doel]
```

## Veelvoorkomende Opties
- `-m <max_hops>`: Stelt het maximale aantal hops in dat traceroute6 zal volgen.
- `-p <poort>`: Specificeert de poort die moet worden gebruikt voor de traceroute.
- `-w <timeout>`: Bepaalt de tijd (in seconden) die moet worden gewacht op een antwoord van elke hop.
- `-n`: Voorkomt dat de opdracht de hostnamen van de IP-adressen probeert op te lossen, wat de snelheid kan verhogen.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `traceroute6`:

1. Basis traceroute naar een IPv6-adres:
   ```bash
   traceroute6 2001:4860:4860::8888
   ```

2. Traceren met een maximum van 15 hops:
   ```bash
   traceroute6 -m 15 2001:4860:4860::8888
   ```

3. Traceren naar een domeinnaam met het oplossen van IP-adressen uitgeschakeld:
   ```bash
   traceroute6 -n google.com
   ```

4. Traceren met een specifieke poort:
   ```bash
   traceroute6 -p 80 2001:4860:4860::8888
   ```

5. Traceren met een aangepaste timeout van 2 seconden:
   ```bash
   traceroute6 -w 2 2001:4860:4860::8888
   ```

## Tips
- Gebruik de `-n` optie als je snelheid wilt verhogen en geen behoefte hebt aan hostnamen.
- Experimenteer met de `-m` optie om te zien hoeveel hops er zijn tussen jouw machine en de bestemming.
- Controleer altijd of je netwerkconfiguratie correct is ingesteld voor IPv6 om nauwkeurige resultaten te krijgen.