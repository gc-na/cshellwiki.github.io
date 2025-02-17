# [Linux] Bash sha512sum gebruik: Bereken SHA-512 hash waarden

## Overzicht
De `sha512sum` opdracht wordt gebruikt om de SHA-512 hash waarde van bestanden te berekenen. Dit is nuttig voor het verifiëren van de integriteit van bestanden en het vergelijken van gegevens.

## Gebruik
De basis syntaxis van de `sha512sum` opdracht is als volgt:

```bash
sha512sum [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-b`: Behandel de invoer als binaire bestanden.
- `-c`: Controleer de hashwaarden van bestanden met een gegeven checksum bestand.
- `-h`: Toon een korte helptekst met informatie over het gebruik van de opdracht.

## Veelvoorkomende Voorbeelden

1. **Bereken de SHA-512 hash van een bestand:**

   ```bash
   sha512sum bestand.txt
   ```

2. **Sla de hashwaarde op in een bestand:**

   ```bash
   sha512sum bestand.txt > hash.txt
   ```

3. **Controleer de hashwaarde met een checksum bestand:**

   Eerst maak je een bestand met de hashwaarden:

   ```bash
   sha512sum bestand.txt > hash.txt
   ```

   Vervolgens controleer je de hash:

   ```bash
   sha512sum -c hash.txt
   ```

4. **Bereken de hash van meerdere bestanden:**

   ```bash
   sha512sum bestand1.txt bestand2.txt
   ```

## Tips
- Zorg ervoor dat je de hashwaarden opslaat in een veilig bestand als je ze later wilt gebruiken voor verificatie.
- Gebruik de `-c` optie om eenvoudig te controleren of bestanden zijn gewijzigd door hun hashwaarden te vergelijken met eerder opgeslagen waarden.
- Het is een goed idee om de hashwaarden te berekenen voor belangrijke bestanden voordat je ze verplaatst of archiveert.