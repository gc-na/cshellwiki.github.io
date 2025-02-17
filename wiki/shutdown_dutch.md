# [Linux] Bash shutdown gebruik: Schakel het systeem uit of herstart het

## Overzicht
De `shutdown`-opdracht in Bash wordt gebruikt om een Linux-systeem veilig uit te schakelen of opnieuw op te starten. Het biedt een manier om het systeem af te sluiten met een waarschuwing voor ingelogde gebruikers, zodat ze hun werk kunnen opslaan.

## Gebruik
De basis syntaxis van de `shutdown`-opdracht is als volgt:

```bash
shutdown [opties] [tijd] [bericht]
```

## Veelvoorkomende Opties
- `-h` : Schakel het systeem uit.
- `-r` : Herstart het systeem.
- `-t` : Stel de tijd in voor het afsluiten (bijvoorbeeld `+5` voor vijf minuten later).
- `now` : Voer de opdracht onmiddellijk uit.
- `+tijd` : Geef een vertraging aan in minuten (bijvoorbeeld `+10` voor tien minuten later).
- `hh:mm` : Specificeer een exacte tijd (bijvoorbeeld `22:00` voor 10 uur 's avonds).
- `-c` : Annuleer een eerder geplande shutdown.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `shutdown`-opdracht:

1. **Systeem onmiddellijk uitschakelen:**
   ```bash
   shutdown -h now
   ```

2. **Systeem herstarten na 5 minuten:**
   ```bash
   shutdown -r +5
   ```

3. **Systeem uitschakelen om 22:00:**
   ```bash
   shutdown -h 22:00
   ```

4. **Systeem herstarten met een bericht:**
   ```bash
   shutdown -r +1 "Systeem wordt herstart voor onderhoud."
   ```

5. **Een geplande shutdown annuleren:**
   ```bash
   shutdown -c
   ```

## Tips
- Zorg ervoor dat je ingelogd bent als root of gebruik `sudo` om de `shutdown`-opdracht uit te voeren.
- Gebruik de `-h` optie voor een veilige uitschakeling van het systeem om gegevensverlies te voorkomen.
- Informeer gebruikers over een geplande shutdown door een bericht toe te voegen, zodat ze hun werk kunnen opslaan.
- Test de opdracht in een veilige omgeving voordat je deze op een productie-systeem uitvoert.