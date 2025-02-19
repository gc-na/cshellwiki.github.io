# [Linux] C Shell (csh) sftp gebruik: Bestanden veilig overdragen

## Overzicht
De `sftp` (Secure File Transfer Protocol) opdracht wordt gebruikt om bestanden veilig over te dragen tussen computers via een netwerk. Het biedt een veilige manier om bestanden te uploaden en downloaden door gebruik te maken van SSH (Secure Shell).

## Gebruik
De basis syntaxis van de `sftp` opdracht is als volgt:

```csh
sftp [opties] [gebruikersnaam@host]
```

## Veelvoorkomende Opties
- `-b batchfile`: Voer opdrachten uit vanuit een batchbestand.
- `-C`: Schakel compressie in voor de overdracht.
- `-P port`: Specificeer een alternatieve poort voor de verbinding.
- `-o option`: Specificeer een extra SSH-optie.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `sftp` opdracht:

1. Verbinden met een remote server:
   ```csh
   sftp gebruiker@voorbeeld.com
   ```

2. Uploaden van een bestand naar de server:
   ```csh
   put lokaal_bestand.txt
   ```

3. Downloaden van een bestand van de server:
   ```csh
   get remote_bestand.txt
   ```

4. Uploaden van een hele directory:
   ```csh
   put -r lokale_map
   ```

5. Downloaden van een hele directory:
   ```csh
   get -r remote_map
   ```

## Tips
- Zorg ervoor dat je de juiste gebruikersnaam en hostnaam gebruikt om verbinding te maken.
- Gebruik de `-C` optie voor snellere overdrachten, vooral bij grote bestanden.
- Controleer altijd de bestandsrechten na het uploaden of downloaden van bestanden om ervoor te zorgen dat ze correct zijn ingesteld.