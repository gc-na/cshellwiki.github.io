# [Linux] C Shell (csh) ftp gebruik: Bestanden overdragen via het netwerk

## Overzicht
De `ftp`-opdracht in C Shell (csh) wordt gebruikt om bestanden over te dragen tussen computers via het File Transfer Protocol (FTP). Het stelt gebruikers in staat om verbinding te maken met een FTP-server, bestanden te uploaden en te downloaden.

## Gebruik
De basis syntaxis van de `ftp`-opdracht is als volgt:

```csh
ftp [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-v`: Verbose modus; toont gedetailleerde informatie over de overdracht.
- `-n`: Voorkomt automatische login bij de FTP-server.
- `-g`: Schakelt globbing uit, wat betekent dat speciale tekens zoals `*` niet worden uitgebreid.
- `-i`: Schakelt interactieve modus uit, waardoor bestanden zonder bevestiging worden overgedragen.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `ftp`-opdracht:

1. Verbinden met een FTP-server:
   ```csh
   ftp ftp.example.com
   ```

2. Bestanden downloaden van de server:
   ```csh
   get bestand.txt
   ```

3. Bestanden uploaden naar de server:
   ```csh
   put lokaal_bestand.txt
   ```

4. Lijst van bestanden op de server weergeven:
   ```csh
   ls
   ```

5. Afsluiten van de FTP-sessie:
   ```csh
   bye
   ```

## Tips
- Zorg ervoor dat je de juiste inloggegevens hebt voordat je verbinding maakt met de FTP-server.
- Gebruik de `-v` optie voor meer inzicht in de overdracht, vooral als je problemen ondervindt.
- Overweeg om een veilige variant van FTP, zoals SFTP, te gebruiken voor gevoelige gegevensoverdracht.