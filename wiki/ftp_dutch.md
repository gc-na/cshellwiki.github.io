# [Linux] Bash ftp gebruik: Bestanden overdragen via het FTP-protocol

## Overview
De `ftp` (File Transfer Protocol) opdracht wordt gebruikt om bestanden over te dragen tussen een client en een server via het FTP-protocol. Het stelt gebruikers in staat om verbinding te maken met een FTP-server, bestanden te uploaden, te downloaden en te beheren.

## Usage
De basis syntaxis van de `ftp` opdracht is als volgt:

```bash
ftp [opties] [argumenten]
```

## Common Options
Hier zijn enkele veelvoorkomende opties voor de `ftp` opdracht:

- `-i`: Zet de interactieve modus uit, zodat bestanden zonder bevestiging worden overgedragen.
- `-v`: Zet de verbose modus aan, zodat gedetailleerde informatie over de overdracht wordt weergegeven.
- `-n`: Voorkomt dat ftp automatisch verbinding maakt met de standaardserver.
- `-p`: Gebruik passieve modus voor de verbinding, wat nuttig kan zijn achter firewalls.

## Common Examples
Hier zijn enkele praktische voorbeelden van het gebruik van de `ftp` opdracht:

1. Verbinden met een FTP-server:
   ```bash
   ftp ftp.example.com
   ```

2. Uploaden van een bestand naar de server:
   ```bash
   put lokaal_bestand.txt
   ```

3. Downloaden van een bestand van de server:
   ```bash
   get server_bestand.txt
   ```

4. Lijst van bestanden op de server weergeven:
   ```bash
   ls
   ```

5. Afsluiten van de FTP-sessie:
   ```bash
   bye
   ```

## Tips
- Zorg ervoor dat je de juiste inloggegevens hebt voordat je verbinding maakt met de FTP-server.
- Gebruik de `-i` optie als je meerdere bestanden wilt uploaden zonder bevestiging.
- Controleer altijd de bestandspermissies na het uploaden of downloaden van bestanden om ervoor te zorgen dat ze correct zijn ingesteld.