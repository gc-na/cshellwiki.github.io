# [Linux] C Shell (csh) scp gebruik: Bestanden veilig kopiëren tussen systemen

## Overzicht
De `scp` (secure copy) opdracht wordt gebruikt om bestanden veilig te kopiëren tussen een lokale en een externe host, of tussen twee externe hosts. Het maakt gebruik van SSH (Secure Shell) voor de overdracht, wat zorgt voor encryptie en beveiliging van de gegevens.

## Gebruik
De basis syntaxis van de `scp` opdracht is als volgt:

```csh
scp [opties] [bron] [doel]
```

## Veelvoorkomende opties
- `-r`: Kopieer mappen recursief.
- `-P [poort]`: Specificeer een andere poort voor de SSH-verbinding.
- `-i [sleutel]`: Gebruik een specifieke SSH-sleutel voor authenticatie.
- `-v`: Zet de uitvoer in verbose modus voor meer gedetailleerde informatie tijdens de overdracht.

## Veelvoorkomende voorbeelden
1. **Een bestand kopiëren van lokaal naar een externe host:**
   ```csh
   scp /pad/naar/lokaal_bestand.txt gebruiker@externe_host:/pad/naar/doelmap/
   ```

2. **Een bestand kopiëren van een externe host naar lokaal:**
   ```csh
   scp gebruiker@externe_host:/pad/naar/externe_bestand.txt /pad/naar/lokale_map/
   ```

3. **Een map recursief kopiëren naar een externe host:**
   ```csh
   scp -r /pad/naar/lokale_map gebruiker@externe_host:/pad/naar/doelmap/
   ```

4. **Een bestand kopiëren met een specifieke poort:**
   ```csh
   scp -P 2222 /pad/naar/lokaal_bestand.txt gebruiker@externe_host:/pad/naar/doelmap/
   ```

## Tips
- Zorg ervoor dat je de juiste machtigingen hebt op de externe host om bestanden te kunnen kopiëren.
- Gebruik de `-v` optie om problemen met de verbinding of overdracht te diagnosticeren.
- Overweeg het gebruik van SSH-sleutels voor een veiligere en gemakkelijkere authenticatie in plaats van wachtwoorden.