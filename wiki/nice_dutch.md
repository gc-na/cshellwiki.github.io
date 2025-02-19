# [Linux] C Shell (csh) nice gebruik: Beheer van procesprioriteit

## Overzicht
De `nice` opdracht in C Shell (csh) wordt gebruikt om de prioriteit van processen te beheren. Hiermee kun je de CPU-tijd die aan een proces wordt toegewezen, verhogen of verlagen, wat nuttig is om de prestaties van verschillende processen te optimaliseren.

## Gebruik
De basis syntaxis van de `nice` opdracht is als volgt:

```csh
nice [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-n` : Hiermee kun je de prioriteit van het proces instellen. Een hogere waarde betekent een lagere prioriteit.
- `-1` tot `19` : Positieve waarden verhogen de prioriteit, terwijl negatieve waarden (bijvoorbeeld `-20` tot `-1`) de prioriteit verlagen.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van de `nice` opdracht:

1. **Een proces met standaard prioriteit starten:**
   ```csh
   nice myscript.sh
   ```

2. **Een proces met verhoogde prioriteit starten:**
   ```csh
   nice -n -5 myscript.sh
   ```

3. **Een proces met verlaagde prioriteit starten:**
   ```csh
   nice -n 10 myscript.sh
   ```

4. **De huidige prioriteit van een proces controleren:**
   ```csh
   ps -o pid,ni,cmd | grep myscript.sh
   ```

## Tips
- Gebruik `nice` om ervoor te zorgen dat belangrijke processen voldoende CPU-tijd krijgen, vooral op systemen met meerdere gebruikers.
- Wees voorzichtig met het verlagen van de prioriteit van kritieke systeemprocessen, omdat dit de algehele systeemprestaties kan beïnvloeden.
- Combineer `nice` met andere opdrachten zoals `nohup` om processen op de achtergrond te draaien zonder dat ze worden onderbroken.