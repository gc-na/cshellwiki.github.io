# [Linux] C Shell (csh) expr gebruik: Voer expressies uit en berekeningen

## Overzicht
De `expr`-opdracht in C Shell (csh) wordt gebruikt om eenvoudige berekeningen uit te voeren en expressies te evalueren. Het kan worden gebruikt voor wiskundige berekeningen, stringmanipulatie en logische vergelijkingen.

## Gebruik
De basis syntaxis van de `expr`-opdracht is als volgt:

```csh
expr [opties] [argumenten]
```

## Veelvoorkomende Opties
- `+` : Optelling van twee getallen.
- `-` : Aftrekking van twee getallen.
- `*` : Vermenigvuldiging van twee getallen.
- `/` : Deling van twee getallen.
- `%` : Modulus (rest) van twee getallen.
- `=` : Vergelijking van twee waarden.
- `:` : Stringlengte.

## Veelvoorkomende Voorbeelden

### Voorbeeld 1: Optelling
```csh
expr 5 + 3
```
Dit geeft `8` als resultaat.

### Voorbeeld 2: Aftrekking
```csh
expr 10 - 4
```
Dit geeft `6` als resultaat.

### Voorbeeld 3: Vermenigvuldiging
```csh
expr 7 \* 6
```
Dit geeft `42` als resultaat. (Let op de escape-teken voor de sterretje.)

### Voorbeeld 4: Deling
```csh
expr 20 / 4
```
Dit geeft `5` als resultaat.

### Voorbeeld 5: Stringlengte
```csh
expr length "Hallo Wereld"
```
Dit geeft `12` als resultaat, de lengte van de string.

### Voorbeeld 6: Vergelijking
```csh
expr 5 = 5
```
Dit geeft `1` (waar) als resultaat, omdat de waarden gelijk zijn.

## Tips
- Vergeet niet om de operatoren correct te escapen, vooral de vermenigvuldigingsoperator (`*`).
- Gebruik haakjes om de volgorde van bewerkingen te bepalen, bijvoorbeeld: `expr \( 5 + 3 \) \* 2`.
- `expr` retourneert altijd een string, dus wees voorzichtig met het interpreteren van de resultaten in scripts.