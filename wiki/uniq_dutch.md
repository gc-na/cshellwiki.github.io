# [Linux] Bash uniq gebruik: Verwijder dubbele regels uit een bestand

## Overzicht
De `uniq` opdracht in Bash wordt gebruikt om dubbele regels in een tekstbestand te verwijderen. Het is handig voor het filteren van gegevens en het vereenvoudigen van uitvoer door alleen unieke regels weer te geven.

## Gebruik
De basis syntaxis van de `uniq` opdracht is als volgt:

```bash
uniq [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-c`: Tel het aantal keren dat elke unieke regel voorkomt.
- `-d`: Toon alleen de regels die meer dan eens voorkomen.
- `-u`: Toon alleen de unieke regels (die slechts één keer voorkomen).
- `-i`: Negeer hoofdlettergebruik bij het vergelijken van regels.

## Veelvoorkomende Voorbeelden

1. **Verwijder dubbele regels uit een bestand:**
   ```bash
   uniq bestand.txt
   ```

2. **Tel het aantal keren dat elke unieke regel voorkomt:**
   ```bash
   uniq -c bestand.txt
   ```

3. **Toon alleen de regels die meer dan eens voorkomen:**
   ```bash
   uniq -d bestand.txt
   ```

4. **Toon alleen unieke regels:**
   ```bash
   uniq -u bestand.txt
   ```

5. **Negeer hoofdlettergebruik bij het vergelijken:**
   ```bash
   uniq -i bestand.txt
   ```

## Tips
- Zorg ervoor dat het bestand gesorteerd is voordat je `uniq` gebruikt, anders worden dubbele regels mogelijk niet correct herkend.
- Combineer `uniq` met de `sort` opdracht voor een efficiënte manier om unieke regels te extraheren:
  ```bash
  sort bestand.txt | uniq
  ```
- Gebruik de `-c` optie om snel een overzicht te krijgen van hoe vaak elke regel voorkomt, wat nuttig kan zijn voor gegevensanalyse.