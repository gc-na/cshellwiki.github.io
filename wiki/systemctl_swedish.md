# [Linux] Bash systemctl användning: Hantera systemtjänster

## Översikt
`systemctl` är ett kommandoradsverktyg som används för att kontrollera systemd-system och tjänster. Det gör det möjligt att starta, stoppa, aktivera och inaktivera tjänster samt hantera systemets tillstånd.

## Användning
Den grundläggande syntaxen för `systemctl` är:

```bash
systemctl [alternativ] [argument]
```

## Vanliga alternativ
- `start`: Startar en tjänst.
- `stop`: Stoppar en tjänst.
- `restart`: Startar om en tjänst.
- `status`: Visar status för en tjänst.
- `enable`: Aktiverar en tjänst så att den startar automatiskt vid systemstart.
- `disable`: Inaktiverar en tjänst så att den inte startar automatiskt vid systemstart.
- `list-units`: Visar en lista över aktiva enheter.

## Vanliga exempel
Här är några praktiska exempel på hur man använder `systemctl`:

1. **Starta en tjänst**
   ```bash
   sudo systemctl start apache2
   ```

2. **Stoppa en tjänst**
   ```bash
   sudo systemctl stop apache2
   ```

3. **Starta om en tjänst**
   ```bash
   sudo systemctl restart apache2
   ```

4. **Kontrollera status för en tjänst**
   ```bash
   systemctl status apache2
   ```

5. **Aktivera en tjänst vid systemstart**
   ```bash
   sudo systemctl enable apache2
   ```

6. **Inaktivera en tjänst vid systemstart**
   ```bash
   sudo systemctl disable apache2
   ```

7. **Lista alla aktiva enheter**
   ```bash
   systemctl list-units --type=service
   ```

## Tips
- Använd `sudo` för att köra `systemctl` med administratörsrättigheter, eftersom många operationer kräver det.
- Kontrollera alltid statusen för en tjänst efter att ha startat eller stoppat den för att säkerställa att åtgärden lyckades.
- Använd `--quiet` alternativet för att dölja onödig utdata om du bara vill ha en bekräftelse på att kommandot kördes.