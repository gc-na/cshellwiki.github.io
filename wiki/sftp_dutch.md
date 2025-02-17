# [Linux] Bash sftp gebruik: Bestanden veilig overdragen

## Overzicht
De `sftp` (Secure File Transfer Protocol) opdracht wordt gebruikt om bestanden veilig over te dragen tussen een lokale en een externe computer via SSH (Secure Shell). Het biedt een veilige manier om bestanden te verzenden en te ontvangen, met encryptie voor de gegevensoverdracht.

## Gebruik
De basis syntaxis van de `sftp` opdracht is als volgt:

```bash
sftp [opties] [gebruikersnaam@]host
```

## Veelvoorkomende Opties
- `-P port`: Specificeert de poort die gebruikt moet worden voor de verbinding.
- `-i identity_file`: Geeft het pad op naar een specifieke privésleutel voor authenticatie.
- `-o option`: Stelt specifieke SSH opties in, zoals `-o StrictHostKeyChecking=no`.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `sftp`:

1. Verbinden met een externe server:
   ```bash
   sftp gebruiker@voorbeeld.com
   ```

2. Bestanden uploaden naar de server:
   ```bash
   put lokaal_bestand.txt
   ```

3. Bestanden downloaden van de server:
   ```bash
   get server_bestand.txt
   ```

4. Een hele map uploaden:
   ```bash
   put -r lokale_map/
   ```

5. Lijst met bestanden op de server bekijken:
   ```bash
   ls
   ```

## Tips
- Zorg ervoor dat je SSH-toegang hebt tot de server voordat je `sftp` gebruikt.
- Gebruik de `-P` optie als de server een andere poort dan de standaardpoort 22 gebruikt.
- Maak gebruik van de `-i` optie om je verbinding te beveiligen met een privésleutel.
- Controleer altijd de integriteit van bestanden na het overdragen, vooral bij grote bestanden.