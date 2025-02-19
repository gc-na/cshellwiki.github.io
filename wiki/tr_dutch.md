# [Linux] C Shell (csh) tr <Gebruik: teksttransformatie>

## Overzicht
De `tr` (translate) opdracht in C Shell wordt gebruikt om tekens in tekst te vertalen of te verwijderen. Het is een krachtig hulpmiddel voor het manipuleren van tekstbestanden en het aanpassen van de inhoud van de uitvoer.

## Gebruik
De basis syntaxis van de `tr` opdracht is als volgt:

```csh
tr [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-d`: Verwijdert de opgegeven tekens uit de invoer.
- `-s`: Vervangt opeenvolgende herhalingen van een teken door één exemplaar.
- `-c`: Specificeert complementaire tekens, wat betekent dat het de tekens die niet zijn opgegeven, verwerkt.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `tr`:

1. **Verander kleine letters naar hoofdletters**:
   ```csh
   echo "hallo wereld" | tr 'a-z' 'A-Z'
   ```

2. **Verwijder spaties uit een tekst**:
   ```csh
   echo "hallo wereld" | tr -d ' '
   ```

3. **Vervang meerdere spaties door een enkele spatie**:
   ```csh
   echo "hallo    wereld" | tr -s ' '
   ```

4. **Verander cijfers naar een ander teken**:
   ```csh
   echo "12345" | tr '0-9' '#'
   ```

## Tips
- Gebruik `tr` in combinatie met andere commando's zoals `cat` of `grep` voor meer geavanceerde tekstverwerking.
- Wees voorzichtig met het gebruik van de `-d` optie, omdat het tekens permanent uit de uitvoer verwijdert.
- Test je `tr` commando's met eenvoudige invoer voordat je ze toepast op grotere bestanden om onbedoelde gegevensverlies te voorkomen.