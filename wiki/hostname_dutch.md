# [Linux] Bash hostname gebruik: Toont of stelt de naam van de host in

## Overzicht
De `hostname` opdracht in Bash wordt gebruikt om de naam van de computer (host) weer te geven of in te stellen. Dit kan nuttig zijn voor netwerkconfiguraties en identificatie van systemen binnen een netwerk.

## Gebruik
De basis syntaxis van de `hostname` opdracht is als volgt:

```bash
hostname [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-a`, `--alias`: Toont de alias van de host.
- `-d`, `--domain`: Toont de domeinnaam van de host.
- `-f`, `--fqdn`: Toont de volledig gekwalificeerde domeinnaam (FQDN).
- `-i`, `--ip-address`: Toont het IP-adres van de host.
- `-s`, `--short`: Toont alleen de korte naam van de host.

## Veelvoorkomende Voorbeelden

1. **Toon de huidige hostnaam:**
   ```bash
   hostname
   ```

2. **Toon de volledig gekwalificeerde domeinnaam:**
   ```bash
   hostname -f
   ```

3. **Toon het IP-adres van de host:**
   ```bash
   hostname -i
   ```

4. **Stel een nieuwe hostnaam in:**
   ```bash
   sudo hostname nieuwe-naam
   ```

5. **Toon de domeinnaam van de host:**
   ```bash
   hostname -d
   ```

## Tips
- Gebruik `sudo` om de hostnaam te wijzigen, aangezien dit meestal beheerdersrechten vereist.
- Vergeet niet om de netwerkservices opnieuw te starten na het wijzigen van de hostnaam voor een correcte werking.
- Controleer altijd de huidige hostnaam met `hostname` voordat je wijzigingen aanbrengt om verwarring te voorkomen.