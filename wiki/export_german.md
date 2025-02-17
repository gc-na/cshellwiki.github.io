# [Linux] Bash export Verwendung: Umgebungsvariablen festlegen

## Übersicht
Der Befehl `export` wird in Bash verwendet, um Umgebungsvariablen zu erstellen oder zu ändern, sodass sie für alle nachfolgenden Prozesse verfügbar sind. Dies ist besonders nützlich, wenn Sie Variablen in Skripten oder in der Shell-Umgebung setzen möchten.

## Verwendung
Die grundlegende Syntax des `export`-Befehls lautet:

```bash
export [Optionen] [Argumente]
```

## Häufige Optionen
- `-p`: Zeigt alle exportierten Variablen an.
- `-n`: Entfernt die Exportmarkierung von Variablen, sodass sie nicht mehr in untergeordnete Prozesse exportiert werden.

## Häufige Beispiele

### Beispiel 1: Eine einfache Umgebungsvariable setzen
Um eine Umgebungsvariable zu setzen und sie für nachfolgende Prozesse verfügbar zu machen, verwenden Sie:

```bash
export MEINE_VARIABLE="Hallo Welt"
```

### Beispiel 2: Überprüfen der exportierten Variablen
Um alle exportierten Variablen anzuzeigen, können Sie den Befehl mit der `-p` Option verwenden:

```bash
export -p
```

### Beispiel 3: Exportieren einer Variablen und gleichzeitiges Ausführen eines Befehls
Sie können eine exportierte Variable auch in einem Befehl verwenden:

```bash
export MEINE_VARIABLE="Hallo Welt" && echo $MEINE_VARIABLE
```

### Beispiel 4: Entfernen der Exportmarkierung
Um die Exportmarkierung von einer Variablen zu entfernen, verwenden Sie:

```bash
export -n MEINE_VARIABLE
```

## Tipps
- Stellen Sie sicher, dass Sie Variablen mit `export` setzen, wenn Sie möchten, dass sie in untergeordneten Prozessen verfügbar sind.
- Verwenden Sie `export -p`, um eine Übersicht über alle aktuell exportierten Variablen zu erhalten.
- Seien Sie vorsichtig beim Überschreiben von bestehenden Variablen, da dies zu unerwartetem Verhalten führen kann.