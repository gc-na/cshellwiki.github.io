# [Linux] Bash switch Verwendung: Schaltet zwischen verschiedenen Optionen um

## Übersicht
Der `switch` Befehl in Bash wird verwendet, um zwischen verschiedenen Optionen oder Fällen zu wechseln. Er ermöglicht es, verschiedene Bedingungen zu überprüfen und entsprechend zu handeln, was die Programmierung von Skripten vereinfacht.

## Verwendung
Die grundlegende Syntax des `switch` Befehls sieht folgendermaßen aus:

```bash
switch [optionen] [argumente]
```

## Häufige Optionen
- `-c`: Führt einen bestimmten Fall aus.
- `-d`: Setzt einen Standardfall, der ausgeführt wird, wenn keine anderen Bedingungen erfüllt sind.
- `-h`: Zeigt die Hilfe und die verfügbaren Optionen an.

## Häufige Beispiele
Hier sind einige praktische Beispiele für die Verwendung des `switch` Befehls:

### Beispiel 1: Einfache Fallunterscheidung
```bash
case $variable in
    wert1)
        echo "Fall 1 ausgewählt"
        ;;
    wert2)
        echo "Fall 2 ausgewählt"
        ;;
    *)
        echo "Standardfall"
        ;;
esac
```

### Beispiel 2: Mehrere Bedingungen
```bash
case $farbe in
    rot)
        echo "Die Farbe ist rot"
        ;;
    blau)
        echo "Die Farbe ist blau"
        ;;
    grün)
        echo "Die Farbe ist grün"
        ;;
    *)
        echo "Unbekannte Farbe"
        ;;
esac
```

### Beispiel 3: Verwendung von Variablen
```bash
case $tag in
    Montag)
        echo "Heute ist Montag"
        ;;
    Freitag)
        echo "Heute ist Freitag"
        ;;
    *)
        echo "Ein anderer Tag"
        ;;
esac
```

## Tipps
- Verwenden Sie klare und aussagekräftige Variablennamen, um die Lesbarkeit Ihres Codes zu verbessern.
- Stellen Sie sicher, dass Sie den Standardfall (`*`) immer am Ende der Fallunterscheidung hinzufügen, um unerwartete Eingaben zu behandeln.
- Testen Sie Ihre Skripte gründlich, um sicherzustellen, dass alle möglichen Fälle abgedeckt sind.