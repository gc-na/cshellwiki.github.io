# [Linux] Bash systemctl gebruik: Beheer van systeemdiensten

## Overzicht
De `systemctl` opdracht is een essentieel hulpmiddel in Linux-systemen voor het beheren van systeemdiensten en het controleren van de status van deze diensten. Het maakt deel uit van het systemd-init-systeem en biedt een uniforme manier om services te starten, stoppen, herstarten en hun status te controleren.

## Gebruik
De basis syntaxis van de `systemctl` opdracht is als volgt:

```bash
systemctl [opties] [argumenten]
```

## Veelvoorkomende opties
- `start`: Start een opgegeven service.
- `stop`: Stop een actieve service.
- `restart`: Herstart een service.
- `status`: Toon de huidige status van een service.
- `enable`: Zet een service aan om automatisch te starten bij het opstarten van het systeem.
- `disable`: Voorkom dat een service automatisch start bij het opstarten van het systeem.
- `list-units`: Toon een lijst van actieve eenheden (services, sockets, etc.).

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `systemctl`:

1. **Een service starten:**
   ```bash
   sudo systemctl start apache2
   ```

2. **Een service stoppen:**
   ```bash
   sudo systemctl stop apache2
   ```

3. **Een service herstarten:**
   ```bash
   sudo systemctl restart apache2
   ```

4. **De status van een service controleren:**
   ```bash
   systemctl status apache2
   ```

5. **Een service inschakelen bij opstarten:**
   ```bash
   sudo systemctl enable apache2
   ```

6. **Een service uitschakelen bij opstarten:**
   ```bash
   sudo systemctl disable apache2
   ```

7. **Lijst van actieve eenheden tonen:**
   ```bash
   systemctl list-units --type=service
   ```

## Tips
- Gebruik `sudo` voor opdrachten die root-toegang vereisen, zoals starten of stoppen van services.
- Controleer regelmatig de status van belangrijke services om ervoor te zorgen dat ze correct functioneren.
- Maak gebruik van de `--quiet` optie om minder uitvoer te krijgen bij het uitvoeren van opdrachten.
- Gebruik `systemctl list-units --failed` om snel te zien welke services zijn mislukt.