# [Linux] Bash hexdump gebruik: Toon de hexadecimale weergave van bestanden

## Overzicht
De `hexdump`-opdracht in Bash wordt gebruikt om de hexadecimale weergave van bestanden te genereren. Dit is handig voor het analyseren van binaire bestanden of het debuggen van gegevens.

## Gebruik
De basis syntaxis van de `hexdump`-opdracht is als volgt:

```bash
hexdump [opties] [argumenten]
```

## Veelvoorkomende opties
- `-C`: Toon de uitvoer in een 'canonical' formaat, wat betekent dat het zowel de hexadecimale waarden als de ASCII-waarden weergeeft.
- `-n <aantal>`: Beperk de uitvoer tot het opgegeven aantal bytes.
- `-v`: Toon alle bytes, zelfs als ze herhaald worden.
- `-e <format>`: Specificeer een aangepaste uitvoerindeling.

## Veelvoorkomende voorbeelden

1. **Basis hexdump van een bestand**:
   ```bash
   hexdump bestand.bin
   ```

2. **Hexdump met ASCII-weergave**:
   ```bash
   hexdump -C bestand.bin
   ```

3. **Beperk de uitvoer tot de eerste 16 bytes**:
   ```bash
   hexdump -n 16 bestand.bin
   ```

4. **Toon alle bytes, inclusief herhalingen**:
   ```bash
   hexdump -v bestand.bin
   ```

5. **Gebruik een aangepaste uitvoerindeling**:
   ```bash
   hexdump -e '16/1 "%02x " "\n"' bestand.bin
   ```

## Tips
- Gebruik de `-C` optie voor een gemakkelijk leesbare uitvoer, vooral als je ook de ASCII-waarden wilt zien.
- Experimenteer met de `-e` optie om specifieke formaten te genereren die passen bij je behoeften.
- Houd rekening met de bestandsgrootte; voor grote bestanden kan het handig zijn om de uitvoer te beperken met de `-n` optie om de leesbaarheid te verbeteren.