# [Linux] Bash killall gebruik: Beëindig processen op basis van naam

## Overzicht
De `killall` opdracht in Bash wordt gebruikt om processen te beëindigen op basis van hun naam. Dit is handig wanneer je meerdere instanties van een programma wilt afsluiten zonder de specifieke proces-ID's (PID's) te hoeven kennen.

## Gebruik
De basis syntaxis van de `killall` opdracht is als volgt:

```bash
killall [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-u`: Beëindig alleen processen die aan een specifieke gebruiker toebehoren.
- `-i`: Vraag bevestiging voordat een proces wordt beëindigd.
- `-s`: Specificeer een signaal dat naar de processen moet worden gestuurd (standaard is dit SIGTERM).
- `-v`: Toon gedetailleerde uitvoer van de processen die worden beëindigd.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `killall`:

1. Beëindig alle instanties van het programma `firefox`:
   ```bash
   killall firefox
   ```

2. Beëindig alle processen die aan de gebruiker `jan` toebehoren:
   ```bash
   killall -u jan
   ```

3. Beëindig een proces met een specifiek signaal, bijvoorbeeld SIGKILL:
   ```bash
   killall -s SIGKILL firefox
   ```

4. Vraag om bevestiging voordat je een proces beëindigt:
   ```bash
   killall -i firefox
   ```

5. Toon gedetailleerde uitvoer van de processen die worden beëindigd:
   ```bash
   killall -v firefox
   ```

## Tips
- Gebruik de `-i` optie om per ongeluk beëindigen van belangrijke processen te voorkomen.
- Controleer altijd welke processen je gaat beëindigen met `ps` of `pgrep` voordat je `killall` gebruikt.
- Wees voorzichtig met het gebruik van `killall` op systemen met meerdere gebruikers, om te voorkomen dat je andermans processen beëindigt.