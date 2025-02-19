# [Linux] C Shell (csh) iostat gebruik: Monitoren van systeeminvoer- en uitvoerstatistieken

## Overzicht
De `iostat`-opdracht wordt gebruikt om statistieken over invoer- en uitvoeractiviteiten van schijven en CPU's te monitoren. Het helpt systeembeheerders bij het analyseren van de prestaties van het systeem en het identificeren van mogelijke knelpunten.

## Gebruik
De basis syntaxis van de `iostat`-opdracht is als volgt:

```csh
iostat [opties] [argumenten]
```

## Veelvoorkomende opties
- `-c`: Toon alleen CPU-statistieken.
- `-d`: Toon alleen schijfstatistieken.
- `-x`: Toon uitgebreide schijfstatistieken.
- `-h`: Gebruik een leesbare indeling voor de uitvoer.
- `interval`: Geef de tijdsinterval in seconden tussen de rapportages aan.
- `count`: Geef het aantal rapportages aan dat moet worden weergegeven.

## Veelvoorkomende voorbeelden

1. **Basisgebruik zonder opties:**
   ```csh
   iostat
   ```

2. **Toon alleen CPU-statistieken:**
   ```csh
   iostat -c
   ```

3. **Toon schijfstatistieken met een interval van 5 seconden:**
   ```csh
   iostat -d 5
   ```

4. **Toon uitgebreide schijfstatistieken:**
   ```csh
   iostat -x
   ```

5. **Toon schijfstatistieken in een leesbare indeling:**
   ```csh
   iostat -d -h
   ```

## Tips
- Gebruik de `-h` optie om de uitvoer gemakkelijker te lezen, vooral bij grote getallen.
- Combineer opties om gerichte informatie te verkrijgen, zoals `iostat -c -d`.
- Monitor regelmatig de prestaties van je systeem om knelpunten tijdig te identificeren en op te lossen.