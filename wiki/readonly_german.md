# [Linux] Bash readonly Verwendung: Variablen schreibgeschützt machen

## Übersicht
Der Befehl `readonly` in Bash wird verwendet, um Variablen als schreibgeschützt zu markieren. Einmal als readonly gesetzt, können diese Variablen nicht mehr verändert oder gelöscht werden, was hilfreich ist, um wichtige Werte während der Ausführung eines Skripts zu schützen.

## Verwendung
Die grundlegende Syntax des Befehls lautet:

```bash
readonly [options] [arguments]
```

## Häufige Optionen
- `-p`: Gibt eine Liste aller readonly-Variablen und deren Werte aus.

## Häufige Beispiele

### Beispiel 1: Eine Variable als readonly setzen
```bash
my_var="Hallo Welt"
readonly my_var
```
In diesem Beispiel wird die Variable `my_var` auf "Hallo Welt" gesetzt und anschließend als readonly markiert.

### Beispiel 2: Versuch, eine readonly-Variable zu ändern
```bash
my_var="Hallo Welt"
readonly my_var
my_var="Neue Werte"  # Dies führt zu einem Fehler
```
Hier wird ein Fehler ausgegeben, wenn versucht wird, `my_var` zu ändern, da sie als readonly festgelegt wurde.

### Beispiel 3: Auflisten aller readonly-Variablen
```bash
readonly -p
```
Dieser Befehl zeigt alle derzeit als readonly markierten Variablen und deren Werte an.

## Tipps
- Verwenden Sie `readonly` für Variablen, die nicht verändert werden sollen, um unbeabsichtigte Fehler zu vermeiden.
- Überprüfen Sie regelmäßig die Liste der readonly-Variablen mit `readonly -p`, um sicherzustellen, dass wichtige Werte geschützt bleiben.
- Beachten Sie, dass readonly-Variablen nur im aktuellen Shell-Kontext gelten.