# [Linux] Bash scp gebruik: Bestanden veilig kopiëren tussen systemen

## Overzicht
De `scp` (secure copy) opdracht wordt gebruikt om bestanden veilig te kopiëren tussen lokale en externe systemen via SSH (Secure Shell). Het biedt een eenvoudige manier om gegevens over een netwerk te verplaatsen met encryptie voor extra veiligheid.

## Gebruik
De basis syntaxis van de `scp` opdracht is als volgt:

```bash
scp [opties] [bron] [doel]
```

## Veelvoorkomende Opties
- `-r`: Kopieert mappen recursief.
- `-P`: Specificeert de poort voor de SSH-verbinding (let op: dit is een hoofdletter P).
- `-i`: Geeft een specifieke identiteitsbestand (SSH-sleutel) op voor authenticatie.
- `-v`: Verhoogt de uitvoer voor debugging en toont gedetailleerde informatie over de overdracht.

## Veelvoorkomende Voorbeelden
1. **Een bestand kopiëren van lokaal naar een externe server:**
   ```bash
   scp /pad/naar/lokaal_bestand.txt gebruiker@server:/pad/naar/doel/
   ```

2. **Een bestand kopiëren van een externe server naar lokaal:**
   ```bash
   scp gebruiker@server:/pad/naar/externe_bestand.txt /pad/naar/lokaal/
   ```

3. **Een hele map kopiëren naar een externe server:**
   ```bash
   scp -r /pad/naar/lokale_map gebruiker@server:/pad/naar/doel/
   ```

4. **Een bestand kopiëren met een specifieke poort:**
   ```bash
   scp -P 2222 /pad/naar/lokaal_bestand.txt gebruiker@server:/pad/naar/doel/
   ```

5. **Een bestand kopiëren met een specifieke SSH-sleutel:**
   ```bash
   scp -i /pad/naar/ssh_sleutel gebruiker@server:/pad/naar/externe_bestand.txt /pad/naar/lokaal/
   ```

## Tips
- Zorg ervoor dat je de juiste permissies hebt op de doelserver om bestanden te kunnen kopiëren.
- Gebruik de `-v` optie voor meer inzicht in eventuele problemen tijdens de overdracht.
- Voor grote bestanden of mappen kan het handig zijn om de overdracht op de achtergrond uit te voeren met `nohup` of `screen`.