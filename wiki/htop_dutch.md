# [Linux] Bash htop gebruik: Procesbeheer en systeemmonitoring

## Overzicht
De `htop` opdracht is een interactieve procesviewer voor Unix-systemen. Het biedt een real-time overzicht van de actieve processen, het gebruik van systeembronnen en andere belangrijke systeeminformatie. In tegenstelling tot de traditionele `top`-opdracht, biedt `htop` een gebruiksvriendelijke interface met kleurcodering en de mogelijkheid om processen eenvoudig te beheren.

## Gebruik
De basis syntaxis van de `htop` opdracht is als volgt:

```bash
htop [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-h`, `--help`: Toont de helpinformatie voor htop.
- `-s`, `--sort`: Sorteert de weergegeven processen op basis van een opgegeven kolom.
- `-p`, `--pid`: Toont alleen de processen met de opgegeven PID.
- `-u`, `--user`: Toont alleen de processen die aan een specifieke gebruiker zijn toegewezen.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `htop`:

1. Gewoon `htop` uitvoeren om de procesviewer te openen:
   ```bash
   htop
   ```

2. `htop` uitvoeren en processen sorteren op gebruik van CPU:
   ```bash
   htop -s PERCENT_CPU
   ```

3. Alleen de processen van een specifieke gebruiker weergeven:
   ```bash
   htop -u gebruikersnaam
   ```

4. Specifieke processen bekijken met een bepaalde PID:
   ```bash
   htop -p 1234
   ```

## Tips
- Gebruik de pijltjestoetsen om door de processen te navigeren en `F9` om een proces te beëindigen.
- Druk op `F2` om de instellingen van htop aan te passen, zoals het kleurenschema en de weergave-instellingen.
- Maak gebruik van de zoekfunctie met `F3` om snel een specifiek proces te vinden.
- Vergeet niet dat `htop` root-rechten nodig kan hebben voor het bekijken van alle processen, dus overweeg om het met `sudo` uit te voeren als dat nodig is.