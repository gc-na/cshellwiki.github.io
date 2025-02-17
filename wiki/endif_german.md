# [Linux] Bash endif Verwendung: Bedingte Anweisungen beenden

## Übersicht
Der `endif`-Befehl wird in Bash-Skripten verwendet, um bedingte Anweisungen zu beenden, die mit `if`-Anweisungen beginnen. Er ist Teil der Kontrollflussstruktur in Bash und sorgt dafür, dass der Code nach einer Bedingung korrekt abgeschlossen wird.

## Verwendung
Die grundlegende Syntax des Befehls ist:

```bash
endif
```

## Häufige Optionen
Der `endif`-Befehl hat keine spezifischen Optionen, da er einfach dazu dient, eine `if`-Bedingung abzuschließen.

## Häufige Beispiele

### Beispiel 1: Einfache Bedingung
```bash
if [ "$USER" == "admin" ]; then
    echo "Willkommen, Admin!"
endif
```

### Beispiel 2: Bedingung mit else
```bash
if [ "$USER" == "admin" ]; then
    echo "Willkommen, Admin!"
else
    echo "Zugriff verweigert."
endif
```

### Beispiel 3: Mehrere Bedingungen
```bash
if [ -f "datei.txt" ]; then
    echo "Die Datei existiert."
elif [ -d "verzeichnis" ]; then
    echo "Das Verzeichnis existiert."
else
    echo "Weder die Datei noch das Verzeichnis existieren."
endif
```

## Tipps
- Achten Sie darauf, dass jede `if`-Anweisung mit einem `endif` abgeschlossen wird, um Syntaxfehler zu vermeiden.
- Verwenden Sie Einrückungen, um die Lesbarkeit Ihres Codes zu verbessern, insbesondere bei komplexen Bedingungen.
- Testen Sie Ihre Skripte gründlich, um sicherzustellen, dass alle Bedingungen wie erwartet funktionieren.