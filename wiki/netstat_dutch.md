# [Linux] Bash netstat gebruik: Netwerkverbindingen en statistieken weergeven

## Overzicht
De `netstat`-opdracht is een krachtig hulpmiddel in de Bash-shell dat informatie geeft over netwerkverbindingen, routingtabellen, interface-statistieken en meer. Het helpt gebruikers bij het analyseren van netwerkactiviteit en het oplossen van netwerkproblemen.

## Gebruik
De basis syntaxis van de `netstat`-opdracht is als volgt:

```bash
netstat [opties] [argumenten]
```

## Veelvoorkomende opties
Hier zijn enkele veelgebruikte opties voor de `netstat`-opdracht:

- `-a`: Toont alle verbindingen en luisterende poorten.
- `-t`: Toont alleen TCP-verbindingen.
- `-u`: Toont alleen UDP-verbindingen.
- `-n`: Toont adressen en poorten in numerieke vorm in plaats van namen.
- `-l`: Toont alleen de verbindingen die aan het luisteren zijn.
- `-p`: Toont het proces dat de verbinding heeft opgezet.

## Veelvoorkomende voorbeelden

1. **Toon alle actieve verbindingen:**

   ```bash
   netstat -a
   ```

2. **Toon alleen TCP-verbindingen:**

   ```bash
   netstat -t
   ```

3. **Toon alleen luisterende poorten:**

   ```bash
   netstat -l
   ```

4. **Toon verbindingen met numerieke adressen:**

   ```bash
   netstat -n
   ```

5. **Toon processen die de verbindingen gebruiken:**

   ```bash
   netstat -p
   ```

## Tips
- Gebruik `netstat -tuln` om een overzicht te krijgen van alle actieve TCP- en UDP-verbindingen die aan het luisteren zijn, met numerieke adressen.
- Combineer opties voor meer gedetailleerde informatie, bijvoorbeeld `netstat -tunlp` om alle actieve verbindingen met procesinformatie te zien.
- Houd er rekening mee dat `netstat` mogelijk niet standaard is geïnstalleerd op alle Linux-distributies; in dat geval kun je `ss` als alternatief gebruiken voor soortgelijke functionaliteit.