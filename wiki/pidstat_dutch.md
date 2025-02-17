# [Linux] Bash pidstat Gebruik: Monitoren van processtatistieken

## Overzicht
Het `pidstat` commando is een handig hulpmiddel in Linux dat gedetailleerde statistieken over actieve processen biedt. Het maakt deel uit van de `sysstat`-pakket en helpt gebruikers om de CPU- en geheugenbelasting per proces te analyseren.

## Gebruik
De basis syntaxis van het `pidstat` commando is als volgt:

```bash
pidstat [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`: Toont een help-bericht met informatie over de beschikbare opties.
- `-p <pid>`: Specificeert de proces-ID (PID) waarvan je de statistieken wilt bekijken.
- `-r`: Toont geheugenstatistieken voor processen.
- `-u`: Toont CPU-gebruikstatistieken voor processen.
- `-d`: Toont I/O-statistieken voor processen.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `pidstat`:

1. **Basis CPU-gebruik per proces bekijken:**
   ```bash
   pidstat
   ```

2. **Statistieken voor een specifieke PID (bijvoorbeeld PID 1234) bekijken:**
   ```bash
   pidstat -p 1234
   ```

3. **CPU-gebruik met geheugenstatistieken tonen:**
   ```bash
   pidstat -r -u
   ```

4. **Statistieken om de 5 seconden verzamelen:**
   ```bash
   pidstat 5
   ```

5. **I/O-statistieken voor een specifieke PID bekijken:**
   ```bash
   pidstat -d -p 1234
   ```

## Tips
- Gebruik `pidstat` in combinatie met andere monitoringtools zoals `top` of `htop` voor een completer beeld van systeembronnen.
- Probeer verschillende opties uit om specifieke informatie te krijgen die je nodig hebt voor probleemoplossing.
- Houd rekening met de frequentie van het verzamelen van gegevens, vooral bij systemen met veel processen, om overbelasting van de uitvoer te voorkomen.