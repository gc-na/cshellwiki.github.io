# [Linux] Bash foreach Verwendung: Schleifen über eine Liste von Elementen

## Übersicht
Der `foreach`-Befehl wird in Bash nicht direkt unterstützt, aber er kann durch die Verwendung von Schleifen wie `for` simuliert werden. Mit `for` können Sie über eine Liste von Elementen iterieren und für jedes Element einen Befehl ausführen.

## Verwendung
Die grundlegende Syntax des `for`-Befehls in Bash sieht folgendermaßen aus:

```bash
for variable in [Liste]; do
    [Befehl]
done
```

## Häufige Optionen
- `in`: Gibt die Liste der Elemente an, über die iteriert werden soll.
- `do`: Leitet den Beginn des Befehlsblocks ein, der für jedes Element ausgeführt wird.
- `done`: Beendet den Befehl.

## Häufige Beispiele

### Beispiel 1: Einfache Schleife über Zahlen
```bash
for i in {1..5}; do
    echo "Zahl: $i"
done
```

### Beispiel 2: Schleife über eine Liste von Dateien
```bash
for file in *.txt; do
    echo "Verarbeite Datei: $file"
done
```

### Beispiel 3: Schleife mit einer Befehlsausgabe
```bash
for user in $(cat users.txt); do
    echo "Benutzer: $user"
done
```

## Tipps
- Verwenden Sie geschweifte Klammern `{}` für eine einfache Generierung von Zahlen oder Buchstaben.
- Achten Sie darauf, dass Sie Variablen in Anführungszeichen setzen, um Probleme mit Leerzeichen oder Sonderzeichen zu vermeiden.
- Nutzen Sie `break` und `continue`, um die Schleife zu steuern, falls notwendig.