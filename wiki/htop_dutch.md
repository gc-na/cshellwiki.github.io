# [Linux] C Shell (csh) htop gebruik: Procesbeheer en systeemmonitoring

## Overzicht
De `htop`-opdracht is een interactieve procesviewer voor Unix-systemen. Het biedt een dynamische weergave van de systeemprocessen, geheugen- en CPU-gebruik, en stelt gebruikers in staat om processen te beheren en te monitoren op een gebruiksvriendelijke manier.

## Gebruik
De basis syntaxis van de `htop`-opdracht is als volgt:

```csh
htop [opties] [argumenten]
```

## Veelvoorkomende opties
- `-h`, `--help`: Toont de helpinformatie voor htop.
- `-s`, `--sort`: Sorteert de weergegeven processen op basis van een opgegeven kolom (bijvoorbeeld `PID`, `CPU`, `MEM`).
- `-p`, `--pid`: Toont alleen de processen met de opgegeven PID's.
- `-u`, `--user`: Toont alleen de processen die door de opgegeven gebruiker worden uitgevoerd.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `htop`:

1. Start htop zonder opties:
   ```csh
   htop
   ```

2. Sorteer processen op CPU-gebruik:
   ```csh
   htop -s PERCENT_CPU
   ```

3. Toon alleen processen van een specifieke gebruiker:
   ```csh
   htop -u gebruikersnaam
   ```

4. Toon processen met specifieke PID's:
   ```csh
   htop -p 1234,5678
   ```

## Tips
- Gebruik de sneltoetsen binnen htop, zoals `F3` om te zoeken naar processen en `F9` om een proces te beëindigen.
- Pas de weergave aan door op `F2` te drukken en de instellingen te configureren naar jouw voorkeur.
- Houd rekening met de sorteeropties om snel inzicht te krijgen in welke processen de meeste middelen gebruiken.