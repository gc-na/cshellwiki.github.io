# [Linux] Bash trap Verwendung: Behandeln von Signalen und Fehlern

## Overview
Der `trap` Befehl in Bash wird verwendet, um bestimmte Aktionen auszuführen, wenn das Skript ein Signal empfängt oder einen Fehler auftritt. Dies ist besonders nützlich, um Ressourcen freizugeben oder um sicherzustellen, dass bestimmte Bereinigungsaktionen durchgeführt werden, bevor das Skript beendet wird.

## Usage
Die grundlegende Syntax des `trap` Befehls lautet:

```bash
trap [Aktion] [Signal]
```

## Common Options
- `EXIT`: Führt die angegebene Aktion aus, wenn das Skript beendet wird.
- `SIGINT`: Reagiert auf das Interrupt-Signal (z.B. Strg+C).
- `SIGTERM`: Reagiert auf das Terminationssignal.
- `ERR`: Führt die angegebene Aktion aus, wenn ein Fehler auftritt.

## Common Examples

### Beispiel 1: Aufräumarbeiten bei Skriptende
```bash
trap 'echo "Skript wird beendet"; rm -f /tmp/tempfile' EXIT
```
In diesem Beispiel wird eine Nachricht ausgegeben und eine temporäre Datei gelöscht, wenn das Skript endet.

### Beispiel 2: Reaktion auf SIGINT
```bash
trap 'echo "Skript unterbrochen"; exit' SIGINT
```
Hier wird eine Nachricht angezeigt und das Skript beendet, wenn der Benutzer Strg+C drückt.

### Beispiel 3: Fehlerbehandlung
```bash
trap 'echo "Ein Fehler ist aufgetreten"; exit 1' ERR
```
In diesem Fall wird eine Fehlermeldung ausgegeben, wenn ein Fehler im Skript auftritt.

### Beispiel 4: Mehrere Signale behandeln
```bash
trap 'echo "Signal empfangen"; exit' SIGINT SIGTERM
```
Dieses Beispiel zeigt, wie man auf mehrere Signale gleichzeitig reagieren kann.

## Tips
- Verwenden Sie `trap` am Anfang Ihres Skripts, um sicherzustellen, dass alle Signale und Fehler von Anfang an behandelt werden.
- Testen Sie Ihre `trap`-Befehle gründlich, um sicherzustellen, dass sie wie gewünscht funktionieren, insbesondere bei unerwarteten Fehlern.
- Nutzen Sie `trap` nicht nur für Fehlerbehandlung, sondern auch für allgemeine Aufräumarbeiten, um sicherzustellen, dass Ihr Skript immer in einem sauberen Zustand endet.