# [Linux] Bash readonly gebruik: Beperk variabelen tot alleen-lezen

## Overzicht
De `readonly` opdracht in Bash wordt gebruikt om variabelen als alleen-lezen in te stellen. Dit betekent dat eenmaal gedefinieerde variabelen niet meer kunnen worden gewijzigd of verwijderd, wat nuttig is om de integriteit van belangrijke waarden te waarborgen tijdens het uitvoeren van scripts.

## Gebruik
De basis syntaxis van de `readonly` opdracht is als volgt:

```bash
readonly [opties] [argumenten]
```

## Veelvoorkomende Opties
- `-p`: Toont een lijst van alle alleen-lezen variabelen en hun waarden.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Een variabele instellen als alleen-lezen
```bash
VAR="Dit is een alleen-lezen variabele"
readonly VAR
```

### Voorbeeld 2: Proberen de waarde van een alleen-lezen variabele te wijzigen
```bash
VAR="Nieuwe waarde"  # Dit zal een foutmelding geven
```

### Voorbeeld 3: Lijst van alleen-lezen variabelen weergeven
```bash
readonly -p
```

## Tips
- Gebruik `readonly` voor belangrijke configuratie-instellingen in je scripts om onbedoelde wijzigingen te voorkomen.
- Controleer altijd of een variabele al als alleen-lezen is ingesteld voordat je probeert deze te wijzigen.
- Houd er rekening mee dat alleen-lezen variabelen niet kunnen worden verwijderd met de `unset` opdracht.