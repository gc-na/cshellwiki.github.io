# [Linux] C Shell (csh) sha256sum gebruik: Bereken SHA-256 hashes

## Overzicht
De `sha256sum` opdracht wordt gebruikt om de SHA-256 hash van bestanden te berekenen. Dit is nuttig voor het verifiëren van de integriteit van bestanden en het vergelijken van bestanden op basis van hun hashwaarden.

## Gebruik
De basis syntaxis van de `sha256sum` opdracht is als volgt:

```csh
sha256sum [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-b`: Behandel de invoer als binaire bestanden.
- `-c`: Controleer de hashes van bestanden op basis van een eerder gegenereerde checksum.
- `-o`: Schrijf de output naar een specifiek bestand.
- `--help`: Toon een helpbericht met informatie over het gebruik van de opdracht.

## Veelvoorkomende Voorbeelden

1. **Bereken de SHA-256 hash van een bestand:**
   ```csh
   sha256sum bestand.txt
   ```

2. **Bereken de SHA-256 hash van meerdere bestanden:**
   ```csh
   sha256sum bestand1.txt bestand2.txt
   ```

3. **Controleer de hash met een checksum bestand:**
   ```csh
   sha256sum -c checksums.sha256
   ```

4. **Schrijf de hash naar een bestand:**
   ```csh
   sha256sum bestand.txt > hash.txt
   ```

## Tips
- Gebruik de `-c` optie om de integriteit van gedownloade bestanden te verifiëren met een checksum bestand.
- Voor binaire bestanden, zorg ervoor dat je de `-b` optie gebruikt om correcte resultaten te krijgen.
- Het is een goede gewoonte om hashes te vergelijken na het verplaatsen of kopiëren van bestanden om dataverlies te voorkomen.