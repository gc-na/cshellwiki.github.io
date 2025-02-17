# [Linux] Bash md5sum gebruik: Controleer de integriteit van bestanden

## Overzicht
De `md5sum`-opdracht wordt gebruikt om de MD5-hashwaarde van bestanden te berekenen. Dit is nuttig voor het controleren van de integriteit van bestanden, omdat zelfs een kleine wijziging in de inhoud van een bestand resulteert in een volledig andere hashwaarde.

## Gebruik
De basis syntaxis van de `md5sum`-opdracht is als volgt:

```bash
md5sum [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-b`: Behandel de invoer als binaire bestanden.
- `-c`: Controleer de MD5-hashes van bestanden op basis van een gegeven bestand met hashes.
- `-t`: Behandel de invoer als tekstbestanden.
- `--help`: Toon een helpbericht met informatie over het gebruik van de opdracht.
- `--version`: Toon de versie-informatie van de `md5sum`-opdracht.

## Veelvoorkomende Voorbeelden
Hier zijn enkele praktische voorbeelden van het gebruik van `md5sum`:

1. **Bereken de MD5-hash van een bestand:**

   ```bash
   md5sum bestand.txt
   ```

2. **Bereken de MD5-hash van meerdere bestanden:**

   ```bash
   md5sum bestand1.txt bestand2.txt
   ```

3. **Sla de MD5-hash op in een bestand:**

   ```bash
   md5sum bestand.txt > bestand.md5
   ```

4. **Controleer de MD5-hash van een bestand met een hashbestand:**

   ```bash
   md5sum -c bestand.md5
   ```

5. **Bereken de MD5-hash van een binaire invoer:**

   ```bash
   md5sum -b bestand.bin
   ```

## Tips
- Zorg ervoor dat je de hashwaarden opslaat in een veilig bestand, zodat je deze later kunt gebruiken voor verificatie.
- Gebruik de `-c` optie om snel te controleren of bestanden zijn gewijzigd door hun hashwaarden te vergelijken met een eerder opgeslagen bestand.
- Wees je ervan bewust dat MD5 niet de veiligste hashfunctie is voor cryptografische doeleinden; overweeg andere algoritmen zoals SHA-256 voor gevoelige toepassingen.