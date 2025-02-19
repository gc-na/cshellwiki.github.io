# [Linux] C Shell (csh) at gebruik: Plan taken voor uitvoering

## Overzicht
De `at`-opdracht in C Shell (csh) wordt gebruikt om taken te plannen die op een specifiek tijdstip moeten worden uitgevoerd. Dit is handig voor het automatiseren van taken zonder dat je handmatig hoeft in te grijpen.

## Gebruik
De basis syntaxis van de `at`-opdracht is als volgt:

```
at [opties] [argumenten]
```

## Veelvoorkomende opties
- `-f` : Specificeer een bestand dat de opdrachten bevat die moeten worden uitgevoerd.
- `-l` : Lijst de geplande taken voor de huidige gebruiker.
- `-d` : Verwijder een geplande taak.
- `-m` : Stuur een e-mail naar de gebruiker na uitvoering van de taak.

## Veelvoorkomende voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `at`-opdracht:

1. **Een eenvoudige taak plannen**:
   Plan een taak om een script uit te voeren om 15:00 uur.
   ```bash
   echo "sh /pad/naar/script.sh" | at 15:00
   ```

2. **Een taak plannen voor morgen**:
   Plan een taak om een bestand te kopiëren naar een andere locatie om 10:30 uur morgen.
   ```bash
   echo "cp /pad/naar/brondocument.txt /pad/naar/doeldocument.txt" | at 10:30 tomorrow
   ```

3. **Een taak plannen met een bestand**:
   Gebruik een bestand met opdrachten om uit te voeren.
   ```bash
   at -f /pad/naar/opdrachten.txt 14:00
   ```

4. **Lijst geplande taken**:
   Bekijk alle taken die je hebt gepland.
   ```bash
   at -l
   ```

5. **Een taak verwijderen**:
   Verwijder een specifieke taak met het taaknummer.
   ```bash
   at -d 5
   ```

## Tips
- Zorg ervoor dat je de juiste tijdzone instelt om verwarring te voorkomen bij het plannen van taken.
- Gebruik de `-m` optie om een bevestigingsmail te ontvangen na de uitvoering van je taak.
- Controleer regelmatig je geplande taken met `at -l` om te zien wat er op de planning staat.