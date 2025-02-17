# [Linux] Bash sha256sum gebruik: Controleer de integriteit van bestanden

## Overzicht
De `sha256sum` opdracht wordt gebruikt om de SHA-256 hashwaarde van bestanden te berekenen. Dit is nuttig voor het controleren van de integriteit van bestanden en het verifiëren of ze niet zijn gewijzigd of beschadigd.

## Gebruik
De basis syntaxis van de `sha256sum` opdracht is als volgt:

```bash
sha256sum [opties] [argumenten]
```

## Veelvoorkomende opties
- `-b`: Verwerkt bestanden in binaire modus.
- `-c`: Controleert de hashwaarden van bestanden op basis van een gegeven checksum-bestand.
- `-h`: Toont een helpbericht met informatie over het gebruik van de opdracht.
- `--tag`: Voegt een tag toe aan de output, wat handig kan zijn voor compatibiliteit met andere tools.

## Veelvoorkomende voorbeelden

1. **Bereken de SHA-256 hash van een bestand:**
   ```bash
   sha256sum voorbeeld.txt
   ```

2. **Bereken de SHA-256 hash van meerdere bestanden:**
   ```bash
   sha256sum bestand1.txt bestand2.txt
   ```

3. **Sla de hashwaarde op in een bestand:**
   ```bash
   sha256sum voorbeeld.txt > hashwaarde.txt
   ```

4. **Controleer de hashwaarde met een checksum-bestand:**
   Eerst maak je een checksum-bestand:
   ```bash
   sha256sum voorbeeld.txt > voorbeeld.sha256
   ```
   Vervolgens controleer je het bestand:
   ```bash
   sha256sum -c voorbeeld.sha256
   ```

## Tips
- Gebruik `sha256sum` in combinatie met andere commando's zoals `find` om de hashwaarden van meerdere bestanden in één keer te berekenen.
- Bewaar de hashwaarden in een veilig bestand om later de integriteit van je bestanden te kunnen controleren.
- Controleer regelmatig de hashwaarden van belangrijke bestanden om ervoor te zorgen dat ze niet zijn gewijzigd.