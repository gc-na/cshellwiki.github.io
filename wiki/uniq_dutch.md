# [Linux] C Shell (csh) uniq gebruik: Verwijder dubbele regels

## Overzicht
Het `uniq` commando in C Shell (csh) wordt gebruikt om dubbele regels in een tekstbestand te verwijderen. Het leest een gesorteerde invoer en geeft alleen unieke regels terug. Dit is handig voor het opschonen van gegevens of het analyseren van tekstbestanden.

## Gebruik
De basis syntaxis van het `uniq` commando is als volgt:

```csh
uniq [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Tel het aantal keren dat elke regel voorkomt.
- `-d`: Geef alleen de regels weer die meer dan eens voorkomen.
- `-u`: Geef alleen de unieke regels weer die slechts één keer voorkomen.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `uniq`:

1. **Verwijder dubbele regels uit een bestand:**
   ```csh
   uniq bestand.txt
   ```

2. **Tel het aantal keren dat elke regel voorkomt:**
   ```csh
   uniq -c bestand.txt
   ```

3. **Toon alleen de regels die meer dan eens voorkomen:**
   ```csh
   uniq -d bestand.txt
   ```

4. **Toon alleen unieke regels:**
   ```csh
   uniq -u bestand.txt
   ```

## Tips
- Zorg ervoor dat de invoer gesorteerd is voordat je `uniq` gebruikt, omdat het alleen werkt met aaneengeschakelde dubbele regels.
- Je kunt `uniq` combineren met andere commando's zoals `sort` om eerst je gegevens te sorteren:
  ```csh
  sort bestand.txt | uniq
  ```
- Gebruik de `-c` optie om snel een overzicht te krijgen van de frequentie van regels in je bestand.