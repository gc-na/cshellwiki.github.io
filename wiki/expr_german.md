# [Linux] C Shell (csh) expr Verwendung: Berechnungen und String-Manipulationen

## Übersicht
Der Befehl `expr` wird in der C Shell verwendet, um einfache mathematische Berechnungen durchzuführen und Zeichenfolgen zu manipulieren. Er kann sowohl arithmetische Ausdrücke als auch logische Vergleiche verarbeiten.

## Verwendung
Die Grundsyntax des Befehls lautet:

```csh
expr [Optionen] [Argumente]
```

## Häufige Optionen
- `+` : Addition von zwei Zahlen.
- `-` : Subtraktion von zwei Zahlen.
- `*` : Multiplikation von zwei Zahlen (muss mit Escape-Zeichen verwendet werden: `\*`).
- `/` : Division von zwei Zahlen.
- `%` : Modulo-Operation (Rest der Division).
- `=` : Vergleicht zwei Werte auf Gleichheit.
- `!=` : Vergleicht zwei Werte auf Ungleichheit.

## Häufige Beispiele

### Beispiel 1: Einfache Addition
```csh
expr 5 + 3
```
Ausgabe: `8`

### Beispiel 2: Subtraktion
```csh
expr 10 - 4
```
Ausgabe: `6`

### Beispiel 3: Multiplikation
```csh
expr 7 \* 6
```
Ausgabe: `42`

### Beispiel 4: Division
```csh
expr 20 / 4
```
Ausgabe: `5`

### Beispiel 5: Modulo
```csh
expr 10 % 3
```
Ausgabe: `1`

### Beispiel 6: String-Länge
```csh
expr length "Hallo Welt"
```
Ausgabe: `11`

### Beispiel 7: String-Konkatenation
```csh
expr "Hallo " : "Hallo \(.*\)"
```
Ausgabe: `0` (Länge des übereinstimmenden Teils)

## Tipps
- Achten Sie darauf, mathematische Operatoren wie `*` mit einem Escape-Zeichen (`\`) zu versehen, um Missverständnisse mit der Shell zu vermeiden.
- Verwenden Sie Klammern, um die Reihenfolge der Berechnungen klarzustellen.
- `expr` gibt nur Ganzzahlen zurück; für Fließkommaoperationen sollten Sie andere Werkzeuge wie `bc` verwenden.