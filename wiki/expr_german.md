# [Linux] Bash expr Verwendung: Berechnungen und Stringvergleiche

## Übersicht
Der `expr` Befehl in Bash wird verwendet, um einfache Berechnungen durchzuführen und Stringvergleiche anzustellen. Er ermöglicht die Auswertung von Ausdrücken und die Rückgabe von Ergebnissen, die in Skripten oder der Kommandozeile weiterverwendet werden können.

## Verwendung
Die grundlegende Syntax des `expr` Befehls sieht wie folgt aus:

```bash
expr [Optionen] [Argumente]
```

## Häufige Optionen
- `+` : Addition von zwei Zahlen.
- `-` : Subtraktion von zwei Zahlen.
- `*` : Multiplikation von zwei Zahlen (muss mit Escape-Zeichen `\*` verwendet werden).
- `/` : Division von zwei Zahlen.
- `%` : Modulo-Operation, gibt den Rest einer Division zurück.
- `=` : Vergleicht zwei Strings auf Gleichheit.
- `!=` : Vergleicht zwei Strings auf Ungleichheit.

## Häufige Beispiele

### 1. Addition
Um zwei Zahlen zu addieren, verwenden Sie:

```bash
expr 5 + 3
```
Ausgabe: `8`

### 2. Subtraktion
Um eine Zahl von einer anderen zu subtrahieren:

```bash
expr 10 - 4
```
Ausgabe: `6`

### 3. Multiplikation
Um zwei Zahlen zu multiplizieren:

```bash
expr 4 \* 2
```
Ausgabe: `8`

### 4. Division
Um eine Zahl durch eine andere zu dividieren:

```bash
expr 20 / 4
```
Ausgabe: `5`

### 5. Modulo
Um den Rest einer Division zu berechnen:

```bash
expr 10 % 3
```
Ausgabe: `1`

### 6. Stringvergleich
Um zwei Strings auf Gleichheit zu überprüfen:

```bash
expr "Hallo" = "Hallo"
```
Ausgabe: `1` (wahr)

### 7. Ungleichheitsvergleich
Um zu prüfen, ob zwei Strings ungleich sind:

```bash
expr "Hallo" != "Welt"
```
Ausgabe: `1` (wahr)

## Tipps
- Achten Sie darauf, Multiplikation mit einem Escape-Zeichen `\*` zu verwenden, um Missverständnisse mit Shell-Wildcards zu vermeiden.
- Nutzen Sie Klammern, um die Reihenfolge der Berechnungen zu steuern, z.B. `expr \( 2 + 3 \) \* 4`.
- `expr` gibt nur Ganzzahlen zurück. Für Fließkommaoperationen sollten andere Tools wie `bc` verwendet werden.