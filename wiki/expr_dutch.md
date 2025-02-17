# [Linux] Bash expr gebruik: Voer berekeningen en stringmanipulaties uit

## Overzicht
De `expr` opdracht in Bash wordt gebruikt voor het uitvoeren van eenvoudige berekeningen en stringmanipulaties. Het kan worden gebruikt om wiskundige expressies te evalueren, strings te vergelijken en substrings te extraheren.

## Gebruik
De basis syntaxis van de `expr` opdracht is als volgt:

```bash
expr [opties] [argumenten]
```

## Veelvoorkomende Opties
- `+` : Optelling van twee getallen.
- `-` : Aftrekking van twee getallen.
- `*` : Vermenigvuldiging van twee getallen (let op: gebruik `\*` om de sterretje te ontsnappen).
- `/` : Deling van twee getallen.
- `%` : Modulus (rest) van twee getallen.
- `=` : Vergelijking van twee waarden.
- `:` : Extractie van een substring.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Optelling
```bash
expr 5 + 3
```
Dit geeft `8` als resultaat.

### Voorbeeld 2: Aftrekking
```bash
expr 10 - 4
```
Dit geeft `6` als resultaat.

### Voorbeeld 3: Vermenigvuldiging
```bash
expr 7 \* 3
```
Dit geeft `21` als resultaat.

### Voorbeeld 4: Deling
```bash
expr 20 / 4
```
Dit geeft `5` als resultaat.

### Voorbeeld 5: Vergelijking
```bash
expr 5 = 5
```
Dit geeft `1` (waar) als resultaat, omdat de waarden gelijk zijn.

### Voorbeeld 6: Substring Extractie
```bash
expr substr "Hallo Wereld" 1 5
```
Dit geeft `Hallo` als resultaat, waarbij de substring vanaf positie 1 van lengte 5 wordt geëxtraheerd.

## Tips
- Vergeet niet om de operator `*` te ontsnappen met een backslash (`\`) om te voorkomen dat deze door de shell wordt geïnterpreteerd.
- Gebruik haakjes om de volgorde van bewerkingen te bepalen, bijvoorbeeld: `expr \( 2 + 3 \) \* 4`.
- `expr` retourneert alleen gehele getallen; voor drijvende getallen zijn er andere tools zoals `bc` nodig.