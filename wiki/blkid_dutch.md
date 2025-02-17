# [Linux] Bash blkid gebruik: Toon schijfpartitie-informatie

## Overzicht
De `blkid`-opdracht in Bash wordt gebruikt om informatie over blokapparaten op een Linux-systeem op te vragen. Het geeft details zoals het bestandssysteemtype, UUID (Universally Unique Identifier) en label van de schijfpartities weer.

## Gebruik
De basis syntaxis van de `blkid`-opdracht is als volgt:

```bash
blkid [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-o, --output`: Bepaalt het uitvoerformaat (bijv. `value`, `full`).
- `-s, --subtype`: Geeft het subtype van het bestandssysteem weer.
- `-p, --probe`: Probeert het apparaat te identificeren, zelfs als het niet is gemonteerd.
- `-c, --cache`: Gebruik een cachebestand voor snellere toegang.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `blkid`:

1. **Toon informatie van alle blokapparaten:**
   ```bash
   blkid
   ```

2. **Toon alleen de UUID's van de schijfpartities:**
   ```bash
   blkid -o value -s UUID
   ```

3. **Toon het bestandssysteemtype van een specifieke partitie:**
   ```bash
   blkid /dev/sda1
   ```

4. **Gebruik de probe-optie om informatie te verkrijgen van een niet-gemonteerd apparaat:**
   ```bash
   blkid -p /dev/sdb
   ```

## Tips
- Gebruik de `-o value` optie om alleen de waarde van een specifiek attribuut te krijgen, wat handig kan zijn voor scripts.
- Controleer regelmatig de UUID's van je partities, vooral na het maken van back-ups of het verplaatsen van gegevens.
- Combineer `blkid` met andere commando's zoals `grep` om specifieke informatie snel te filteren.