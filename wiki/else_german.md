# [Linux] Bash else Verwendung: Bedingte Anweisungen in Skripten

## Übersicht
Der `else` Befehl in Bash wird verwendet, um alternative Anweisungen auszuführen, wenn eine vorherige Bedingung nicht erfüllt ist. Er ist Teil der `if`-Anweisung und ermöglicht es, verschiedene Codepfade basierend auf Bedingungen zu steuern.

## Verwendung
Die grundlegende Syntax des `else` Befehls sieht wie folgt aus:

```bash
if [ Bedingung ]; then
    # Anweisungen, wenn die Bedingung wahr ist
else
    # Anweisungen, wenn die Bedingung falsch ist
fi
```

## Häufige Optionen
Der `else` Befehl selbst hat keine spezifischen Optionen, da er Teil der `if`-Anweisung ist. Die Optionen beziehen sich auf die `if`-Bedingung, die Sie verwenden.

## Häufige Beispiele

### Beispiel 1: Einfache Bedingung
```bash
#!/bin/bash
zahl=10

if [ $zahl -gt 5 ]; then
    echo "Die Zahl ist größer als 5."
else
    echo "Die Zahl ist 5 oder kleiner."
fi
```

### Beispiel 2: Überprüfen einer Datei
```bash
#!/bin/bash
datei="test.txt"

if [ -e $datei ]; then
    echo "Die Datei existiert."
else
    echo "Die Datei existiert nicht."
fi
```

### Beispiel 3: Benutzerabfrage
```bash
#!/bin/bash
echo "Möchten Sie fortfahren? (ja/nein)"
read antwort

if [ "$antwort" == "ja" ]; then
    echo "Fortfahren..."
else
    echo "Abbrechen."
fi
```

## Tipps
- Stellen Sie sicher, dass Sie die `if`-Bedingung korrekt formulieren, um unerwartete Ergebnisse zu vermeiden.
- Verwenden Sie Anführungszeichen um Variablen, um Probleme mit Leerzeichen oder leeren Werten zu vermeiden.
- Testen Sie Ihre Skripte gründlich, um sicherzustellen, dass alle Bedingungen und Alternativen wie gewünscht funktionieren.