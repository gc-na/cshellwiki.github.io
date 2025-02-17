# [Linux] Bash case Verwendung: Mustervergleich in Shell-Skripten

## Übersicht
Der `case` Befehl in Bash wird verwendet, um Mustervergleiche durchzuführen. Er ermöglicht es, verschiedene Bedingungen zu überprüfen und basierend auf dem Ergebnis unterschiedliche Aktionen auszuführen. Dies ist besonders nützlich in Shell-Skripten, um die Lesbarkeit und Struktur zu verbessern.

## Verwendung
Die grundlegende Syntax des `case` Befehls sieht folgendermaßen aus:

```bash
case [variable] in
    [muster1])
        [Befehle]
        ;;
    [muster2])
        [Befehle]
        ;;
    *)
        [Befehle für keinen Treffer]
        ;;
esac
```

## Häufige Optionen
- `*)`: Dies ist ein Platzhalter, der verwendet wird, wenn kein Muster übereinstimmt.
- `;;`: Beendet den aktuellen Fall und signalisiert das Ende der Befehle für diesen Fall.

## Häufige Beispiele

### Beispiel 1: Einfache Fallunterscheidung
```bash
#!/bin/bash
echo "Geben Sie eine Zahl zwischen 1 und 3 ein:"
read zahl

case $zahl in
    1)
        echo "Sie haben 1 eingegeben."
        ;;
    2)
        echo "Sie haben 2 eingegeben."
        ;;
    3)
        echo "Sie haben 3 eingegeben."
        ;;
    *)
        echo "Ungültige Eingabe."
        ;;
esac
```

### Beispiel 2: Überprüfung von Dateitypen
```bash
#!/bin/bash
datei="beispiel.txt"

case $datei in
    *.txt)
        echo "Es handelt sich um eine Textdatei."
        ;;
    *.jpg|*.png)
        echo "Es handelt sich um ein Bild."
        ;;
    *)
        echo "Unbekannter Dateityp."
        ;;
esac
```

### Beispiel 3: Benutzerinteraktion
```bash
#!/bin/bash
echo "Wählen Sie eine Option: (a/b/c)"
read option

case $option in
    a)
        echo "Option A gewählt."
        ;;
    b)
        echo "Option B gewählt."
        ;;
    c)
        echo "Option C gewählt."
        ;;
    *)
        echo "Ungültige Option."
        ;;
esac
```

## Tipps
- Verwenden Sie `*)` am Ende Ihrer `case`-Anweisung, um unerwartete Eingaben zu behandeln.
- Achten Sie darauf, dass die Muster in der Reihenfolge angeordnet sind, in der sie geprüft werden sollen.
- Nutzen Sie die Möglichkeit, mehrere Muster in einer Zeile zu kombinieren, um den Code kompakt zu halten (z.B. `*.jpg|*.png`).

Mit diesen Informationen sind Sie gut gerüstet, um den `case` Befehl effektiv in Ihren Bash-Skripten zu verwenden!